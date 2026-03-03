# Document your edge case here
- To get marks for this section you will need to explain to your tutor:
1) The edge case you identified

I noticed that when updating information of the student, if you leave the optional mark field blank, it automatically sets the score to zero. 
However the intent of emptying the marks field can be ambiguous, the edits may mean to NOT change the score, which is actually more likely then setting it to zero

2) How you have accounted for this in your implementation

From an user experience perspective, because the EditStudentModal is prefilled with the current mark, we expect user to not touch the marks field if they meant to keep it unchanged, and expect users to explictly put in zero if they actually mean it. 

Hence I decided to handle this by making this field required in the modal and users may choose to not modify it at all if they don't mean to.