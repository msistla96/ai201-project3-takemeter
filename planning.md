## Dataset specifications

### Community

The community chosen is the Subreddit r/anime. This has been present since 2008 and provides the most diverse ranges of posts and comments across different types of anime, which allows me to collect a diverse set of data to provide a classifier that can be as accurate as possible.

### Labels

Discussion is a post that invites other people to share, debate, or react to a topic. 
Review is a post that gives a more direct personal judgment of the topic with reasons and usually a clear overall opinion.


### Hard edge cases

1. When a small discussion turns into a full blown analysis.
Decision: If the details can be removed without changing the post's central
claim, it's a discussion. If removing the details changes the central claim,
it's an analysis — even if the post ends with an open question.


### Data collection plan

Reddit archives through Arctic Shift as it's free.
Since it's a large community, there will be sufficient examples for each kind of label that it can be a balanced set.


### Evaluation metrics

## Evaluation results
Per class metrics are important, especially for posts that can be Discussion and Review. This will tell me if it works for on the boundary posts.
Validation loss is also important during fine tuning as training accuracy can reflect overfitting.

### Definition of success

For subjective measures,this kind of tool can help moderators help redirect posts to another thread or channel, post warning labels for spoilers that don't have the tag and prevent unecessary bot activity that pulls away from the threads becoming irrelevant.

Based on this, having an error margin of incorrect labels less than 10% would make it reliable as a classification tool.

## AI tool plan

### Label stress-testing
I will Claude to stress test my definitions and edge cases. 

### Annotation Assistance
Use AI to prelabel all the examples. A quick way for me to verify is to pull up examples per label, split them into batches of 10 and validate if they are right or not.

### Failure Analysis
I will ask Claude Code to look at initial metrics and help guide my reporting and fine tuning.
