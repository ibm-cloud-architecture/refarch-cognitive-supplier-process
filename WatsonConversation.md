# Watson Conversation Readme

## Base Integration with BPM
The Watson Conversation is connected to our BPM Coach via a simple coachview. This coachview contains a chunk of custom HTML held in an iframe that opens up a window of our simple bluemix microserver that presents a simple interface to the Watson Conversation. The Conversation we are accessing here is the exact same one that you would get when you build your Watson Conversation inside Bluemix and are prompted to download an instance.


## Coachview

![WatsonConversationCV](docs/watson-conversation.png)
As far as the Coachview we simply utilize some SparkUI functionality to trigger a modal's visibility.

The Spark UI Button has this event configuration option set for onClick

`${Modal_Section2}.setVisible(true);`

In this case the `Modal_Section2` is the modal's Control ID

The chunk of custom HTML text inside the modal's content box is listed below

```
    <body>
    <iframe src="https://supplieronboardingconversationnode.mybluemix.net/" width = 400 height =500 allowtransparency="false" style=  'Background : White'>
    </iframe>
    </body>
```
