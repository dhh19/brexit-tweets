# Tweet ids for the #brexit tweets used in the Helsinki Digital Humanities Hackathon 2019

This dataset contains lists of tweet ids for the tweets used as material by the "Brexit in Transna­tional So­cial Me­dia" group in the [Helsinki Digital Humanities Hackathon 2019](http://heldig.fi/dhh19/).

Due to restrictions in Twitter's terms of service, the full tweet dataset cannot be made public. However, Twitter allows the publication of tweet ids, from which the dataset can be reconstituted, _with the exception of deleted tweets_.

The dataset was gathered as follows: Between 2019-01-22T09:19Z and 2019-04-15T14:42Z, a [Twarc](https://github.com/DocNow/twarc) version 1.6.1 script was called hourly to retrieve and archive tweets from Twitter matching the #brexit hashtag using the Twitter search API. All 5,547,585 tweet IDs returned by this run are listed in the file `original_ids.txt.gz`.

However, upon further inspection, problems were identified in the archiving. For an unidentified reason, gathering did not occur between 2019-02-13T06:17Z and 2019-02-26T09:24Z. In addition, the Twarc script had been run without the `--extended` argument, so the tweet data contained only truncated contents for many tweets.

Due to this, a decision was taken to rehydrate a new dataset of tweets falling between 2019-02-26T09:24Z and 2019-04-15T14:42Z. Of the original 4,197,059 tweets gathered for this time period (listed in `continuous_ids.txt`), 3,941,653 could be rehydrated (i.e., they had not been deleted in the interim). The ids of tweets in this dataset are listed in the file `continuous_rehydrated_ids.txt`.

Finally, out of these rehydrated tweets, a subset was derived that filtered out all tweets that were pure retweets. This subset consisted of 1,104,514 tweets, whose ids are listed in the file `continuous_rehydrated_no_retweets_ids.txt`.
