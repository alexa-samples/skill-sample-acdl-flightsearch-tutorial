## Flight Search Tutorial

This is the source code of Building Multiturn Skills with Alexa Conversations by using ACDL tutorial. You can find the details of the skill in the tutorial [https://developer.amazon.com/en-US/docs/alexa/workshops/acdl-flightsearch-tutorial/get-started/index.html](https://developer.amazon.com/en-US/docs/alexa/workshops/acdl-flightsearch-tutorial/get-started/index.html)

**_NOTE:_** This skill is an example only and is not intended to refer to actual airlines or airline data.

### Prerequisites

You need to have:
- An Amazon developer account. If you don't already have one, go to the [ASK Developer Console](https://developer.amazon.com/alexa/console/ask) to create an account.
- An AWS account to host your skill on AWS Lambda. If you don't already have one, go to [AWS](https://aws.amazon.com/account/) to create an IAM user account.


You also need to update your existing software:
- The latest version of [Node.js](https://nodejs.org/en/download/) (version 17.4 or higher)
- [Git](https://git-scm.com/downloads) version control system (version 2.35 or higher)
- [Java](https://www.java.com/en/) development environment (version 1.8 or higher)
- The [Amazon Web Services Command-Line Interface (AWS CLI)](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)

**_NOTE:_** If you haven't used AWS CLI before, you need to configure AWS.


### Install and configure the ASK CLI

#### Step 1: Install the ASK CLI
- From the command line, run the following command:
```
npm install -g ask-cli-x
```

You can uninstall the public version of the ASK CLI (if necessary). From the command line, run the following command:
```
npm uninstall -g ask-cli
```


#### Step 2: Configure the ASK CLI
- To link the ASK CLI with your Amazon developer account and your AWS account, run the following command:
```
askx configure
```

The command you use to run the beta version of the ASK CLI is askx instead of ask. However, command-line messages might refer to ask. For ACDL, always use askx.

##### Configure the ASK CLI

- Choose the default profile or enter a name to create a new profile
**_NOTE:_** This tutorial follows the steps for \"default\" profile. If you choose to create a new profile, you need to explicitly set this profile when you run askx commands. When you initialize your account, you need to run ```askx init -p tutorial``` or when you deploy your skill, you need to run ```askx deploy -p tutorial``` (\"tutorial\" is an example profile, replace it with your profile name).
- Grant permission to link your AWS profile to your ASK CLI skill
  - Sign in to the [AWS Key Management Service (KMS)](https://docs.aws.amazon.com/IAM/latest/UserGuide/console.html) as an IAM user
  - Choose a [symmetric access key.](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#symmetric-cmks) This is a single 256-bit secret encryption key


To troubleshoot configuration issues, see the [ASK CLI quick-start page](https://developer.amazon.com/en-US/docs/alexa/smapi/quick-start-alexa-skills-kit-command-line-interface.html).

#### (Optional) Step 3 Install the ACDL syntax highlighter for VS Code

If you use Visual Studio (VS) Code and want to use the ACDL syntax highlighter, follow the instructions here. ACDL syntax highlighting is currently available only for VS Code.

Install the ACDL syntax highlighter for VS Code

- Make sure you have the latest version of VS Code:
  - Open VS Code and click Help.
  - Click the update-related option, which might be Check for Updates or Restart to Update.

- Install the ASK Toolkit VS Code extension (version 2.10 or higher).

- If you've already the extension installed, update it to the latest version.
  - Open VS Code and click Code > Preferences > Extensions.
  - Search for the Alexa Skills Kit (ASK) toolkit extension.
  - Click the gear icon, and then click Install another version > 2.10.

You can test syntax highlighting by creating a new ACDL file or by opening an ACDL project file.

**_NOTE:_** You still must use the ASK CLI to compile and deploy your skill. The current version of the VS Code toolkit doesn't support ACDL deployment.


## Additional Resources
For more information about ACDL, visit:
- [https://developer.amazon.com/en-US/docs/alexa/conversations/about-acdl.html](https://developer.amazon.com/en-US/docs/alexa/conversations/about-acdl.html)

For more information about Alexa Conversations visit:

- [https://developer.amazon.com/en-US/docs/alexa/conversations/about-alexa-conversations.html](https://developer.amazon.com/en-US/docs/alexa/conversations/about-alexa-conversations.html)
- [https://developer.amazon.com/en-US/blogs/alexa/alexa-skills-kit/2020/07/introducing-alexa-conversations-beta-a-new-ai-driven-approach-to-providing-conversational-experiences-that-feel-more-natural](https://developer.amazon.com/en-US/blogs/alexa/alexa-skills-kit/2020/07/introducing-alexa-conversations-beta-a-new-ai-driven-approach-to-providing-conversational-experiences-that-feel-more-natural)
- [Alexa Conversations Pet Match tutorial](https://developer.amazon.com/en-US/alexa/alexa-skills-kit/get-deeper/tutorials-code-samples/build-multi-turn-skills-with-alexa-conversations)

## Continue the conversation
-	Reach out to the Alexa Developer team on Twitter [@alexadevs](https://twitter.com/alexadevs)
-	Join the Alexa Community slack at [alexa.design/slack](http://alexa.design/slack) to chat with fellow Alexa skill developers.
-	Join the Alexa Developer team for regular streaming programs on Twitch and YouTube, where we regularly dive into advanced voice design concepts and new features of the ASK SDK.
-	Find code and coaching to help you get more proficient with Alexa  features in the following GitHub repositories:
	   - [Alexa](https://github.com/alexa) - SDKs & Complete Skills for supported features
	   - [Alexa-Samples](https://github.com/alexa-samples/) - Code Snippets & Demonstrations
	   - [Alexa-Labs](https://github.com/alexa-labs/) - Try new and experimental features

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the Amazon Software License.

