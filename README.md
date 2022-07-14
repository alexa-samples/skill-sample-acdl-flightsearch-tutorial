## Flight Search Tutorial

### Prerequisites

You need to have:
- An Amazon developer account. If you don't already have one, go to the [ASK Developer Console](https://developer.amazon.com/alexa/console/ask){:target="&lowbar;blank" rel="noopener noreferrer"} to create an account.
- An AWS account to host your skill on AWS Lambda. If you don't already have one, go to [AWS](https://aws.amazon.com/account/){:target="&lowbar;blank" rel="noopener noreferrer"} to create an IAM user account.


You also need to update your existing software:
- The latest version of [Node.js](https://nodejs.org/en/download/){:target="&lowbar;blank" rel="noopener noreferrer"} (version 17.4 or higher)
- [Git](https://git-scm.com/downloads){:target="&lowbar;blank" rel="noopener noreferrer"} version control system (version 2.35 or higher)
- [Java](https://www.java.com/en/){:target="&lowbar;blank" rel="noopener noreferrer"} development environment (version 1.8 or higher)
- The [Amazon Web Services Command-Line Interface (AWS CLI)](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html){:target="&lowbar;blank" rel="noopener noreferrer"}

{% include note.html content="If you haven't used AWS CLI before, you need to configure AWS." %}


### Install and configure the ASK CLI

#### Step 1: Install the ASK CLI
- From the command line, run the following command:
<div id="c1" markdown="block">
{% include copybutton.html id="c1" %}
{% highlight bash %}
npm install -g ask-cli-x
{% endhighlight %}
</div>

{% include image.html file="ask-conversations/npm_install" type="png" alt="nmp install -g ask-cli-x" caption="installation of ask-cli-x" border="true" max-width="80%" %}

{% include note.html content="Uninstall the public version of the ASK CLI (if necessary). From the command line, run the following command:
```
npm uninstall -g ask-cli
```
" %}


#### Step 2: Configure the ASK CLI
- To link the ASK CLI with your Amazon developer account and your AWS account, run the following command:
<div id="c2" markdown="block">
{% include copybutton.html id="c2" %}
{% highlight bash %}
askx configure
{% endhighlight %}
</div>


{% include note.html content="The command you use to run the beta version of the ASK CLI is askx instead of ask. However, command-line messages might refer to ask. For ACDL, always use askx." %}

##### Configure the ASK CLI

- Choose the default profile or enter a name to create a new profile
{% include note.html content="This tutorial follows the steps for \"default\" profile. If you choose to create a new profile, you need to explicitly set this profile when you run askx commands. When you initialize your account, you need to run ```askx init -p tutorial``` or when you deploy your skill, you need to run ```askx deploy -p tutorial``` (\"tutorial\" is an example profile, replace it with your profile name)." %}
- Grant permission to link your AWS profile to your ASK CLI skill
  - Sign in to the [AWS Key Management Service (KMS)](https://docs.aws.amazon.com/IAM/latest/UserGuide/console.html){:target="&lowbar;blank" rel="noopener noreferrer"} as an IAM user
  - Choose a [symmetric access key.](https://docs.aws.amazon.com/kms/latest/developerguide/concepts.html#symmetric-cmks){:target="&lowbar;blank" rel="noopener noreferrer"} This is a single 256-bit secret encryption key

{% include image.html file="ask-conversations/askx_configure" type="png" alt="askx configure" caption="configuring ask cli for ACDL" border="true" max-width="80%" %}

To troubleshoot configuration issues, see the [ASK CLI quick-start page](https://developer.amazon.com/en-US/docs/alexa/smapi/quick-start-alexa-skills-kit-command-line-interface.html){:target="&lowbar;blank" rel="noopener noreferrer"}.

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

{% include note.html content="You still must use the ASK CLI to compile and deploy your skill. The current version of the VS Code toolkit doesn't support ACDL deployment." %}

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the Amazon Software License.

