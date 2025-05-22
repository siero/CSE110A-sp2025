---
title: "Schedule"
layout: splash
---

_I will strive to get slides uploaded before lecture_

_This schedule is tentative, based on previous offerings. We may change topics. We will discuss any changes throughout class and we will keep this schedule up to date_

_Unless explicitly mentioned, Readings will refer to Engineering a Compiler (EAC), see the references [page](https://sorensenucsc.github.io/CSE110A-sp2024/references.html)_


### Module 1: Lexing   

| Date             | Topic    | Slides |   Readings
|------------------|----------|--------|----------------   
| Tue, April 1     | Administrative (v3) | [slides](./PDFS/C110-01A-Admin-v3.pdf) | [Overview page](https://siero.github.io/CSE110A-sp2025/overview.html) |
| 				   | Introduction to Compilers | [slides](./PDFS/C110-01B-Intro2Compilers1.pdf) | 
| 				   | Journey into a Compiler | [slides](./PDFS/C110-02A-Journey-Into-A-Compiler.pdf) | 
| Thu, April 4     | Introduction to Lexical Analysis  | [slides](./PDFS/C110-01C-Intro2Compilers2.pdf) | EAC Chapter 1
| 				   | Lexer: Naive      | [slides](./PDFS/C110-03A-lexers-naive.pdf) | 
|------------------|-------------------|--------------------------------------------|
| Tue, April 8     | Quiz 1: Intro     | [quiz1](./PDFS/Quiz-01-Init-Survey.pdf)                                ||
|                  | Quiz 2: Warnings, Errors, Equivalences | [quiz2](./PDFS/Quiz-02-Warnings-Errors-Equiv.pdf) ||
|------------------|-------------------|----------------------------------------------------|--|
| Thu, April 10    | Quiz-04: RE 	   | [quiz4](./PDFS/Quiz-04-REs.pdf)                    |  |
|                  | Lexer: RE         | [slides](./PDFS/C110-04A-lexers-re.pdf)            |  |
|                  | Lexer: EM-SOS-NG  | [slides](./PDFS/C110-05A-lexers-EM-SOS-NG_v2.pdf)  |  |
|                  | Lexer: lexer-actions | [slides](./PDFS/C110-06A-lexer-actions-v2.pdf)  |  | 
|------------------|------------------------------|-----------------------------------------|--|

### Module 2: Parsing  (Estimated Date) 

| Date             | Topic    | Slides |   Readings
|------------------|----------|--------|----------------
| Thu, April 15    | Quiz-05: EM-SOS-NG-Actions   | [quiz5](/PDFS/Quiz-05-EM-SOS-NG-Scanner-Actions.pdf)  	| EAC Chapter 3.2, 3.3 (first half) |
| 				   | CFG and Ambiguous Grammars   | [slides](PDFS/C110-07A-CFG-Ambig-rev2.pdf)          	| |
| 				   | Precedence and Associativity | [slides](PDFS/C110-09A-PREC-ASSOC-rev2.pdf)         	| |
| Thu, April 17    | Top Down Parsing 			  | [slides](PDFS/C110-10A-TOP-DOWN-PARSING-rev2.pdf) 		| |
| 				   | 							  | [slides](PDFS/C110-10B-TOP-DOWN-PART2-rev1.pdf) 		| | [ply documentation](https://www.dabeaz.com/ply/ply.html) |
|------------------|------------------------------|--------|-------------------------------------------|-|
| Tue, April 22	   | Quiz-06:CFG-AMBIG-PRECEDENCE | [quiz6](PDFS/Quiz-06-CFG-AMBIG-PREC.pdf)           | | 
| 				   | Right and Left Derivations	  | [slides](PDFS/C110-11B-RIGHT-LEFT-DERIVATIONS.pdf) | | 
|				   | Recursive Descent Parsing 	  | [slides](PDFS/C110-11A-RECURSIVE-DESCENT-rev2.pdf) | |
| Thu, April 24    | Scope						  | [slides](PDFS/C110-13A-SCOPE.pdf) 				   | | 
|				   | Review: Top Down, Rec Descent| [slides](PDFS/C110-12B-REVIEW-TOP-DOWN-PART2-rev2.pdf) | |  
|------------------|----------|--------|----------------
| Tue, April 29	   | Quiz-07-AMBIG-TOP-DOWN-REC-DESC (UPDATED) | [quiz7](PDFS/Quiz-07-AMB-TOP-DOWN-REC-DESC.pdf)  | |
|				   | EXAM-MIDTERM-STUDY-GUIDE           | [slides](PDFS/C110-EXAM-MIDTERM-STUDY-GUIDE.pdf) | |
|				   | BOTTOM-UP-PARSING 				    | [slides](PDFS/C110-12D-BOTTOM-UP-PARSING.pdf)       | |
| Thu, May 01      | MIDTERM STUDY GUIDE                | [slides](PDFS/C110-EXAM-MIDTERM-STUDY-GUIDE-rev2.pdf)    | |
|				   | MIDTERM REVIEW / BOTTOM-UP PARSING | [slides](PDFS/C110-MIDTERM-REVIEW.pdf)              | |
|				   | EXAMPLE OF POST-ORDER TRAVERSAL    | [slides](PDFS/C110-POSTORDER-TRAVERSAL-EXAMPLE.pdf) | |
|------------------|------------------------------------|-----------------------------------------------------|-|

### Module 3: Intermediate representations (Estimated Date) 

| Date             | Topic    | Slides |   Readings
|------------------|----------|--------|----------------
| Tue, May 06      | MIDTERM  |        | 
| Thu, May 08      | Abstract Syntax Trees (ASTs) | [slides](PDFS/C110-M3-01-AST.pdf)| EAC Chapter 5.1 | 
|------------------|------------------------------|--------|---------|
| Tue, May 13      | AST and TYPE Systems | Quiz:TBD  | EAC Chapter 4.2 | 
|                  |                      | [slides](PDFS/C110-M3-02-AST-POT-TYPES.pdf)  |   | 
|                  |                      | [slides](PDFS/C110-M3-03-TYPES-FUNCTIONS.pdf)|   | 
| Thu, May 15      | Intermediate Representations (IR) | [slides](PDFS/C110-M3-04-FUNCTIONS-IR-SCOPE_rev3.pdf)| EAC Chapter 5.3 |
|------------------|----------|--------|--------|
| Tue, May 20      | IR Representations (IR) / HW4 | same slides as last Thursday | | | 
|------------------|----------|--------|--------|

### Module 4: Optimization and Other Topics (TBD, Estimated Date)   

| Date             | Topic    | Slides |   Readings
|------------------|----------|--------|----------------
| Thu, May 22      | Quiz-08 TYPE and IR GEN | [Quiz 8](PDFS/Quiz-08-TYPE-AND-IR-GEN.pdf) | |
|                  | Local Optimizations / Basic Blocks | [slides](PDFS/C110-M4-01-OPTIMIZATIONS_rev2.pdf) | EAC Chapter 8.1 |
|------------------|----------|--------|--------|
| Tue, May 27      | <TBD>    | <TBD>  | <TBD> 
| Thu, May 29      | <TBD>    | <TBD>  | <TBD> 
|------------------|----------|--------|----------------
| Tue, May 03      | <TBD>    | <TBD>  | <TBD> 
| Thu, May 05      | <TBD>    | <TBD>  | <TBD> 
|------------------|----------|--------|----------------

## Final

