# QuestionImprovement
Stack Overflow Question Quality Improvement

## Dataset Introduction
This dataset expands the Jie Yang's [work](https://chauff.github.io/documents/publications/HYPER2014-yang.pdf) by adding the answer count for each revision. 

The data is in [__target.csv__](https://github.com/bigheiniu/QuestionImprovement/blob/master/target.csv). The columns in __target.csv__ are as follows:

| Column Name  | Meaning                                                     |
| :----------- | ----------------------------------------------------------- |
| version      | The version of the question. It starts from 1.              |
| Text         | The text of current version of question.                    |
| change type  | The revision type of the question.                          |
| answer_count | The number of answers the question recieved after revision. |
| answer_label | The label of the answer count.                              |

It should be noticed that numeric change type has following map relationship:

| Value | Meaning                             |
| ----- | ----------------------------------- |
| -1    | Spell Problem                       |
| 0     | Explain Code Usage                  |
| 1     | Add Example/URL                     |
| 2     | Code Intervention                   |
| 3     | Add Error Info Stack Trace          |
| 4     | Add Context information (OS system) |
| 5     | Attempt                             |
| 6     | Solution                            |

Answer label is based on the count of answer count. 

- If answer count is 0, the answer label is -1;
- If answer count is 1, the answer label is 0;
- Otherwise, the answer label is 1. 



## Expand the Dataset

You can use search query in [Stack Exchange](https://data.stackexchange.com/) to query more data samples. There are severl examples here:

1. Find raw text and edit text for question, [here](https://data.stackexchange.com/stackoverflow/query/1019161/find-raw-text-and-edit-text-for-question)
2. Find attempt related question intervention, [here](https://data.stackexchange.com/stackoverflow/query/1039640)
3. Find answer count before revision, [here](https://data.stackexchange.com/stackoverflow/query/1039674/find-previous-answer-count)



## TODO

1. Include more data samples. 
