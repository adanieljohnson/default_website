

References for less copy editing and more coaching

Undergraduate introductory STEM courses typically include technical writing training. Often it is treated as an incidental skill that each student develops "along the way." Or, the instructional strategy is  haphazardly designed, implemented, and executed. Adding to the challenge, faculty may not be directly responsible for helping students develop writing skills. 

Technical writing training usually is part of a lab course associated with a lecture class. These lab sections may be be led by graduate teaching assistants or even advanced undergraduates. These instructors may have under-developed writing skills themselves, or lack pedagogical content knowledge needed to guide students effectively. 

In 2014 we launched an automated data collection process we call SAWHET that collects systematic observations and sample data from student writers and graduate instructors. Our resarch goal is to better understand student and instructor behaviors within the technical writing instructional space. Our practical goal is to develop techniques for teaching technical writing that:

*  Can be implemented at large scale by less experienced teaching assistants;
*  Emphasize student development through holistic coaching;
*  Shift student and instructor attention away from simple copy-correction towards larger writing issues; and
*  Embody other best practices outlined in nearly 40 years of research literature on "writing in the disciplines."

We have a structured database of >5000 laboratory reports written by undergraduate students for introductory biology courses. In addition we have all comments that a TA made on the individual reports, plus associated metadata:

*  Context. Was it first or second report of the semester? Initial submission or revision? What course and topic in the course? What year in college was the author?
*  Instructor information. Which TA provided the feedback? What score was assigned, and what what the rationale behind that score?

We are using multiple text-mining methods to map key features of student writing, as well as connections and correlations between those features. These insights then inform how we teach technical writing and train graduate instructors.

####\  

## Context for This Project & Prior Work
Students make greater gains as writers if instructors avoid telling students what to correct ("copy editing"), and use a coaching-oriented approach instead. To that end, we train graduate teaching assistants to use a **global first, specific later** approach to grading undergraduate technical writing. We ask TAs to spend a limited block of time writing fewer comments that focus on broader issues. Ideally, TAs provide no more than 3-5 comments per text page, and comments should encourage student reflection. As students' writing improves, the TA can focus on smaller issues.   

This strategy is well-supported by prior research, but we are uncertain how well TAs can implement the recommended strategy. One of our ongoing questions has been, **"what do TAs ACTUALLY spend most of their time and effort making comments about when they grade student writing?"**

In Summer 2018, we began analyzing TAs' comments from student papers. We extracted and tabulated all comments from approximately 500 pairs of reports (initial submissions and revisions) collected during a single semester in 3 different courses. Initial data cleaning involved removing duplicates, splitting comments addressing multiple independent writing issues, and removing comments lacking any context for judging intent. In all, the final tabulated dataset included ~11,000 separate comments.

We next used a subset of 100 randomly selected comments to build an initial qualitative codebook for sorting comments into types. The initial codebook was re-tested using 1100 additional randomly selected comments. Using the final codebook, we sorted all 11,000 comments into separate categories (see LINK for complete codebook.)

Coded TA comments were sorted on two axes: 

* __Subject__: did the comment focus mainly on Basic criteria, Technical issues, Writing quality, Logic, or Other issues
* __Structure__: was the comment mainly Copy correction, General or Specific information, Pointing to another resource, or Holistic coaching for improvement?

The sorted contingency table provided us with a relative estimate of TA effort.

####\  

## The Central Problem of This Project
Qualitative coding of TA comments is informative but unsustainable. Developing the codebook then rating the first set of 11,000 comments required nearly 2 months of investigator effort. Even with the codebook, individual coders will require training to achieve any accuracy. Given 10-12,000 comments are generate EACH SEMESTER, an automated sorting method is needed.

####\  

# Literature Review
##General Approach to Initial Dataset
The following excerpt from *Text Mining with R: A Tidy Approach* (Julia Silge and David Robinson) summarizes how extended text (in this case, TA comments) can be organized as a tidy matrix.*All emphases are mine.*

>We thus define the tidy text format as being a table with one-token-per-row. A token is a **meaningful unit of text**, such as a word, that we are interested in using for analysis, and tokenization is the process of splitting text into tokens. 

>This one-token-per-row structure is in contrast to the ways text is often stored in current analyses, perhaps as strings or in a document-term matrix. For tidy text mining, the token that is stored in each row is most often a single word, **but can also be an n-gram, sentence, or paragraph** . In the tidytext package, we provide functionality to tokenize by commonly used units of text like these and convert to a one-term-per-row format.

Using tidy format (vs. other common text data formats) better maintains relationships between individual comments and metadata, which simplifies subsequent analysis.
