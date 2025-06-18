# AI Conferences Info for ASReview

This directory contains the information for the conferences in a format that is readily usable in [ASReview](https://asreview.nl/).

## Tips

If you wish to merge and clean the data to use in ASReview, I recommend using [asreview-datatools](https://github.com/asreview/asreview-datatools). Here are some example usage, supposing you have downloaded this repository to a directory `~/repos/`:

### Merge information from conferences from 2023-2025

```bash
asreview data vstack 2023-2025.tsv $(find ~/repos/ai_conferences_info/ -type f -regex ".*202[3-5]\.tsv")
```

### Clean the newly merged file, checking for duplicates with a high similarity between titles and abstracts and saving the result to a clean file 

```bash
asreview data dedup 2023-2025.tsv --similar --verbose -o 2023-2025_clean.tsv
```

