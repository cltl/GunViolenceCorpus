## Gun Violence Corpus

This repository contains the Gun Violence Corpus, described in the publication
[TO INCLUDE]

## Contents

This repository contains three files:
* **system_input.conll**
* **gold.conll**
* **verbose.conll**

Some observations about the file format:
* every document starts with a line starting with #begin document (DOC_ID);
* the line after that always provides the document creation time.
* each line in **system_input.conll** and **gold.conll** consists of four columns: token identifier, token, discourse type (DCT or TITLE or BODY), and (only in gold) coreference chain identifier (default value is a dash '-')
* every document ends with a line #end document
* the file **verbose.conll** has an additional column (inserted as column 4) with more information about the annotation. For more information, we refer to the [annotation guidelines](https://docs.google.com/document/d/1Pkrg_uZcD8l04bilCRSrC5vHpl_HTyDqcuXBY2Dq_GI/edit?usp=sharing). 
The syntax of the verbose annotation is INCIDENT_ID.EVENTTYPE.PARTICIPANT_INFORMATION

Finally, most event coreference evaluation evaluation is performed using 
[this](https://github.com/conll/reference-coreference-scorers) external scorer.
As is the case in our conll files, the external scorer evaluates using the information in the last column.
In addition, the system file and gold file need to have the same amount of columns.
