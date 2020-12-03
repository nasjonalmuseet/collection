# JSON export from Nasjonalmuseet collection (Elastic 7.8.1) 03.12.2020*

Export via Postman, using Elastic Scroll API:
https://www.elastic.co/guide/en/elasticsearch/reference/6.8/search-request-scroll.html

*42 465 objects*
Only object with multimedia/images are included.
Some objects that have more than one photo included in the dataset. The main/default photo can be identified by the parameter `thumbnail` in the `multimedia` part of the metadata.
