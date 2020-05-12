# Slack Get Conversation Steps

This step allows you to get a conversation from a slack channel.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [SlackStepsGetConversation.zip](SlackStepsGetConversation.zip) - Workflow zip file with the step and example flow
* [slack.png](/slack.png) - Slack logo

# How it works
The **Slack - Get Conversation** step gets a conversation from Slack, and can be configured to limit the number of messages and remove bots from conversation.

The **Slack - Beautify Conversation** step takes the output of the **Slack - Get Conversation** step and makes it useable in an xMatters Notification.


# Installation

## Slack Setup
None, just configure the OAuth in xMatters.

## xMatters Setup
1. Download the [SlackStepsGetConversation.zip](SlackStepsGetConversation.zip) file onto your local computer
2. Navigate to the Workflows tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded
4. Create a new endpoint for Slack, and use the Slack endpoint type.


## Usage
The **Slack - Get Conversation** and **Slack - Beautify Conversation** steps are now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **Get Conversation** workflow has a canvas that can be triggered via HTTP call. 

## Slack - Get Conversation

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Channel Name | Yes | 0 | 2000 | The name of the Channel in Slack | | No |
| Max Messages | Yes | 0 | 2000 | How many messages to get | | No |
| Display Apps? | Yes | 0 | 2000 | Whether to get Bots and Apps. Either true or false | | No |
| Blacklist | Yes | 0 | 2000 | Comma-separated list of any uses or bots names that should not be included | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| Conversation | Conversation from channel. |


## Slack - Beautify Conversation

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| Conversation | Yes | 0 | 2000 | Conversation from the **Slack - Get Conversation** Step | | No |
| Time Zone | Yes | 0 | 2000 | Name of timezone (e.g. America/New_York) Find options [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) | | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| result | Beautified conversation |


## Example
This is an example of using both the **Slack - Get Conversation** and **Slack - Beautify Conversation** steps.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

