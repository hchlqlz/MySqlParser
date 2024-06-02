1. The cmd.txt file contains commands for generating C # code.
2. MySQLBaseLexer.cs / MySQLBaseRecognizer.cs: These two files were translated by me from TypeScript file. The source file is located in https://github.com/antlr/grammars-v4/tree/master/sql/mysql/Oracle/TypeScript.
3. MySQLLexer.g4 / MySQLParser.g4: These two files are based on official syntax files, I only made a few changes, the source file is located in https://github.com/antlr/grammars-v4/tree/master/sql/mysql/Oracle. 
---
The problem has been identified. I have rewritten the Text/Type attributes in the MySQLBaseLexer.cs file, which is an incorrect approach. The correct approach would be to modify this.type / this.text to this.Type / this.Text in the syntax file.
