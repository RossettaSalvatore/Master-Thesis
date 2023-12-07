# Master-Thesis

## 17-24/11/23
- Structure of the thesis: introduced Foundation chapter, added bullet points in contribution paragraph.
- Add simple examples to divisor methods and properties.
- Formalization of basic definitions and properties (anonymity and monotonocity).
- Add social choice theory definitions and properties in Foundation chapter.
- Add framework paragraph in Foundation chapter. 

## 29/11/23 - Meeting with Professor Beckert 
- Add monotonocity "variant" property: if a party "A" has more votes than another party "B", then A must have at least the same number of parties than B.
- Change outcome of the module from "Parties => Seats" to "Seats => Parties", assigning each seat to a party.

## 25/11/23-1/12/23
- Fixed Expose after meeting, update thesis stucture: Foundations, Voting Theory, Implementation in Isabelle, Implementation in Framework. 
- Starting working on Isabelle, implementing the first definitions and modules.
- As said in the meeting, Seats is not anymore "'a => nat" assigning number of seats to parties but it is now "nat => 'a": each seat is numbered and assigned to a party ('a). This allows to keep track of every seat and to handle ties.
- First discussion about how to handle ties. They will be handled with alternatives.
- Added "concordance" property according to Pukelsheim Notes.

## 2/12/23-9/12/23
- Change structure of the thesis: the implementation now will be directly on the framework to better check which modules to use.
- look at Loop Composition, Terminal Conditions, Electoral Module, Defer Module which will be used in my work. 
