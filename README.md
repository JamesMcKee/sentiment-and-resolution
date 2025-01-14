# sentiment-and-resolution

Scripts for implementing a generative AI analysis on transcripts of calls to customer support.

Tested on python 3.10.16

Install requirements with: \
pip install -r requirements.txt

* There are a lot of requirements because it was painful getting transformers to work, ended up just pip freezing the environment that worked. If you can find the exact incantation needed to minimally install a working transformers, please let me know!

# model testing
files for this are in the test/ directory \
test/simulated_transcripts was generated with GPT4 to build the sentiment analysis model. Contains 10 files for each combination of positive/negative/neutral sentiment with resolved/not resolved call status. The two test scripts use these files. \
Filenames have the format <sentiment>_<resolution>_<int>.txt

test_if_resolved.ipynb tests various zero shot classifiers to determine the outcome of the call to customer support.

test_sentiment_models.ipynb tests the sentiment of the "Member" side of the conversation.

# using the model
files for this are in the scr/ directory \
find_sentiment_and_resolution.ipynb tests classifies each file in the transcripts directory as positive/negative/neutral member sentiment and whether the call was resolved/not resolved. \
The script also checks for common themes in the resolved and unresolved categories separately, to provide insights into how effective different aspects of customer support are.


# Note
* This comes with absolutely no warranty
* Free software under MIT license
* Please contact James McKee for any questions relating to usage
