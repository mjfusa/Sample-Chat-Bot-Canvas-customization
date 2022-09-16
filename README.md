# Sample: Chat Bot customization - Power Virtual Agents / Bot Framework

## Introduction

The Microsoft documentation: [Customize the look and feel of the bot's default canvas](https://docs.microsoft.com/en-us/power-virtual-agents/customize-default-canvas) describes how to customize the chat bot's canvas. You can change the title, styles for all text elements - background, foreground, font, text, etc. You can also define the icons displayed for the bot and the user. The height and width of the canvas can also be customized.

## Configure the sample

Define the value of **BOT_ID** in files ```Demo.html``` and ```Demo1.html```. See here for instructions on obtaining the **BOT_ID**: [Customize the look and feel of the bot's default canvas](https://docs.microsoft.com/en-us/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters), section 'Retrieve your Power Virtual Agents bot parameters'.


## Run the sample

1) Deploy the contents of the sample to the root of a test web site.
2) Navigate to ```Demo.html```.
3) Scroll down one row and click the 'Chat' button.
4) You will see the chat window appear ready for input. Note the customizations for the chat canvas header.
4) Type 'Hi' to start the bot.
Note the customized bot icon.
 
1) Navigate to ```Demo1.html```.
Repeat steps 1 - 5 above. 
Note the updated customizations.

## How it works

The bot canvas itself is in ```BotPage.html``` (and ```BotPage1.html```). It contents closely follows the documentation [here](https://docs.microsoft.com/en-us/power-virtual-agents/customize-default-canvas).

```Demo.html``` include code to display and hide the **iframe** that displays the bot canvas. Here is the code:

```javascript
<script>
    function openForm() {
    document.getElementById("myForm").style.display = "block";
    }
    function closeForm() {
    document.getElementById("myForm").style.display = "none";
    }
</script>

<button onclick="openForm()" class="open-button">Chat</button>
<div id="myForm" class="chat-popup">
    <iframe src="BotPage.html" frameborder="0" style="width: 100%; height: 100%; background: #FFFFFF;"></iframe>
    <button onclick="closeForm()" class="closePopUp">X</button>
</div>
```




```
