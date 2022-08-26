# Parser
This is a parser implemented in C++.
The syntax definitions of a small programming language, called Pascal-Like Simple Language (PLSL), are given below using EBNF notations. The PLSL syntax has some features similar to the well-known Pascal Language.
1. Prog ::= PROGRAM IDENT; DeclBlock ProgBody
2. DeclBlock ::= VAR {DeclStmt;}
3. DeclStmt ::= Ident {, Ident} : (Integer | Real | String)
4. ProgBody ::= BEGIN {Stmt;} END
5. Stmt ::= AssigStmt | IfStmt | WriteLnStmt | ForStmt
6. WriteLnStmt ::= WRITELN (ExprList)
7. IfStmt ::= IF ( LogicExpr ) THEN Stmt [ELSE Stmt]
8. ForStmt ::= FOR Var := ICONST (TO | DOWNTO) ICONST DO Stmt
9. AssignStmt ::= Var := Expr
10. ExprList ::= Expr {, Expr}
11. Expr ::= Term {(+|-) Term}
12. Term ::= SFactor {( * | / ) SFactor}
13. SFactor ::= [(+ | -)] Factor
14. LogicExpr ::= Expr (= | > | <) Expr
15. Var ::= IDENT
16. Factor ::= IDENT | ICONST | RCONST | SCONST | (Expr) 
