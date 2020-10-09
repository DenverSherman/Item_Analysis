# Item Analysis Workflow Outline
## Research and identify formulae for indeces: Discrimation and Difficulty.

* 1: Outline on the terms to use in Item Analysis, Definitions for Item Difficulty, Item Descrimination, Point Biserial correlation coefficient (PBS), test Score Reliabililty found here !(GuideToItemAnalysis)[http://www.schreyerinstitute.psu.edu/pdf/GuideToItemAnalysis.pdf]

* 2: Sample item analysis !(ScorePak)[https://s3-us-west-2.amazonaws.com/uw-s3-cdn/wp-content/uploads/sites/105/2015/01/24112540/itemanal.pdf]

* 3: University of Kansas !(Item Analysis Guide)[http://www.specialconnections.ku.edu/?q=assessment/quality_test_construction/teacher_tools/item_analysis#:~:text=Divide%20by%20the%20total%20number%20of%20students%20who%20took%20the%20test.&text=Sort%20your%20tests%20by%20total,difficulty%20index%20for%20the%20item.]


## Write in generality for csv input

### Standarized csv input
flubaroo correct answer matrix generated from a google forms assessment (1 response set per student)
This form has a column for each answer, values are 1 for a correct answer and 0 for an incorrect answer


### Difficulty index
Difficulty index : proportion of students who got the item correct (3)

psuedocode:

// D.I. = #correct / #tested
question 1 = {a,b,c,d}
correct_answer = c

df = {student: response}
difficulty_index = len(df[correct_answer])/len(df)

### Discrimination Index
Discrimination Index: A comparison of how overall high scorers on the whole test did on one particular item compared to overall low scorers (3)

let upper be top 50% of students by overall score
let lower be bottom 50% of students by overall score

calculate upper_difficulty_index = UDI
calculate lower_difficulty_index = LDI

discrimination index = UDI - LDI

## Return metrics in a visualisation
