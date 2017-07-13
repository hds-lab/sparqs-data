# Content Analysis Results for SparQs (HCII'17)
This repository contains results from our content analysis on social media literature. You can find our paper [here](http://nanchen.csie.org/publications/SparQs_HCI%20International_2017.pdf).

## Citation
Chen NC. et al. (2017) SparQs: Visual Analytics for Sparking Creativity in Social Media Exploration. In: Meiselwitz G. (eds) Social Computing and Social Media. Applications and Analytics. SCSM 2017. Lecture Notes in Computer Science, vol 10283. Springer, Cham

or please refer to [our publication's page on Springer](https://link.springer.com/chapter/10.1007/978-3-319-58562-8_30) for more other citation format options.

## Files
### full_content_analysis_results.json
This file contains our full analysis results in json. Please refer to our paper for the analysis questions.

The basic format looks like the following:
```
[
{
   "paper": {...},
   "analysis": {...}
},
...
]
```

### rewritten_research_questions.xlsx
This Excel spreadsheet contains the original research questions and the corresponding rewritten questions and extracted dimensions.
Note that the dimension extraction is annotated with numbers, and the numbers refers to the order in the "Dimension(s)" column.
For example, here is one rewritten question:
```
What 123\kind of TV content\ drives Twitter engagement 2\during a show\?	
```
and its corresponding dimensions:
```
Topic; Keywords; Hashtags; Time
```
Therefore, 1 is Topic, 2 is Keywords, and 3 is Time. ``123\kind of TV content\`` means that these words correspond to all the three dimension, whereas ``2\during a show\`` refers to only the Time dimension.

### research_questions.json
This is file where the rewritten research questions are in json format with papers metadata, but without the original research questions.
The numbering approach is the same as the ``rewritten_research_questions.xlsx``.

Here is an example of a paper entry. Note that in the file all the entries are in a list.
```json
  {
        "source":{
            "authors":"Julie Letierce\nAlexandre Passant\nJohn Breslin\nStefan Decker",
            "title":"Understanding how Twitter is used to spread scientific messages",
            "year":"2010",
            "venue":"WebSci10: Extending the Frontiers of Society On-Line"
        },
        "dimensions":[
            "sender_name",
            "keywords",
            "hashtags",
            "location",
            "timezone"
        ],
        "text":"How do 1\\researchers\\ tweet at 2345\\conferences\\?"
    }
```
