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

## 2/12/23-8/12/23
- Change structure of the thesis: the implementation now will be directly on the framework to better check which modules to use.
- Look at Loop Composition, Terminal Conditions, Electoral Module, Defer Module which will be used in my work. 
- Abstraction of Seats from nat => 'a to 'a => 'b; therefore, adaptation of functions developed will be necessary.
- Structure of the divisor module finalized.
- Tie breaking strategy: only in the case of a tie, for the disputed seats I leave not an only element in the set but the alternatives. Example: 0 => A, 1 => B, 2 => {A, B}. 

## 9/12/23-15/12/23
- Finished writing functions to use in the method, like "apply_divisor_module_list" which assigns seats to parties and updates fract-votes entries and "tie_breaking_module", which assigns all tied parties to remaining seats.
- Despite what said in the last week meeting, tie_breaking_module has been implemented with returning one Seats function and not two ("assigned" and "disputed"): this way it's more efficient and I have the same output for both ties and no ties situation.
- Finished to change all types to polymorphic ones: the only one left are nat for counters and lengths and nat list for the parameters but they will be changed.

## 16/12/23-23/12/23
- Single functions written last week put together in bigger submodules.
- Implementation of "main_function", which takes the already counted votes among other parameters and assigns all the seats.
- Now Seats is a 'a => 'b set function: this is due to cleaning of the code and semplification of some types.

## 05/01/24-22/01/24
- Adaptating functions of the module to framework's ones 
- Write theorem about anonyimity
- Starting to write proofs and termination conditions for minor functions (such as find_max_votes)
- Introducing type synonym "Divisor_Module_Params", series of products of parameters

## 23/01/24-
- Changing products type synonym Divisor_Module_Params with a record after Dr. Kirsten's advice
- To this record I added "nseats", number of seats current available
- Subsequent adaptations of all functions to the record
- Cleaning some functions (like main_function)
- Reading documents about locales and starting to introduce it in code: this locale will have both my record and Electoral Module
- Adding lemmas about decreasing measures on functions (divisor_module, loop_divisor, main_function)
