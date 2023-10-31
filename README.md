# PAC
This repository holds the PAC dataset for the EMNLP 2023 paper [Crossing the Aisle: Unveiling Partisan and Counter-Partisan Events in News Reporting](https://arxiv.org/abs/2310.18768).

## Contents
- data/annotations/: final annotations of each story.
- data/train.json: the training split that contains news articles from 2012 - 2021.
- data/dev.json: the development split that contains news articles from 2022 - 2022.06
- data/test.json: the test split that contains news articles from 2022.07 - 2023

The annotation file in `data/annotations/` is formatted as follows:
```
{
  "title":
  "id":
  "split":
  "date":
  "topic":
  "source":
  "media_ideology":
  "relative_ideology":
  "absolute_ideology":
  "news":[{"id":, "text"}...]
  "events":[{"e_id":, "token":, "sentence_id":,"start":, "end":,"remove":,"partisanship":, "entity":}...]
  "entity_list":[{"text":, "ideology":, "id":, "events":[]}...]
}
```
The data JSON file in `data` is formatted as follows:
```
{
  "story_id": [article_1, article_2],...
}
```
## Updates ##
- **(10/31)**: Initial Data Release
- **In Progress**: Release individual annotations and merge entity annotations
