# Installation Guide for the Demo CRM project from the *AAA on an Indie Budget* Presentation

The first thing you'll need is a Google account. If you don't have one, or don't want to use the one you have for this, head on over and [set one up](https://accounts.google.com/signup/v2/webcreateaccount?continue=https%3A%2F%2Faccounts.google.com%2F&flowEntry=SignUp&flowName=GlifWebSignIn).

Once you have created or signed into your Google account, click on [this link](https://docs.google.com/spreadsheets/d/1QGIgTJhRyCvWHR_JetEa_B1mjyCIAv5PtAN3tIFNUjM/edit?usp=sharing) to access my Demo CRM from AAA on an Indie Budget - SourceCon Altanta F'18 template on Google Sheets. You should see something like this:

![demo-crm-to-copy](/Graphics/demo-crm-to-copy.PNG)

Click on the `File` menu, and choose `Make a copy...` from the dropdown, 

![make-a-copy-step1](/Graphics/make-a-copy-step1.png)

rename it if you like, choose where to save it, and hit `OK`. Now you've got your very own copy to work with. Just a few more steps to get it up and running.

If your new file didn't open automatically, go find it in your Drive and make sure you've got it pulled up, as the next few instructions won't work if you're still looking at the `View Only` copy! Yours should look something like this, depending on what you named it:

![new-demo-crm-copy-first-look](/Graphics/new-demo-crm-copy-first-look.PNG)

From top menu, select `Tools`, then `<> Script editor`, 

![tools-script-editor](/Graphics/tools-script-editor.PNG) 

to open up the script editor in a new tab. Your view should now be something like this:

![script-editor-view](/Graphics/script-editor-view.PNG)

This is a view I hope you'll become pretty familiar with soon. The script editor is where we access all the code embedded in the spreadsheet. You're looking at a Google App Script project file. In order to give an App Script project full access to edit and update your Google Sheets file, it needs to be created from the script editor menu. 

Within this project are several sub-files, an `appscript.json` file you should leave alone unless you know what you're doing (I still don't), a `CRM Functions.gs` file that contains all my App Script code, and a series of `.html` files, each containing the HTML code required to show various popups and views used by the CRM. 

`CRM Functions.gs` should be the first file that opens up, but if not, click on it now. You'll notice that it's a pretty long file, perhaps a bit unweildly. You can split your code into as many `.gs` files as you like, I just felt it was easier to keep it in one for distribution purposes. Just make sure you don't duplicate functions between the files, if you split them up!

With the `CRM Functions.gs` file open, click on `Select function` option, and choose `onOpen` from the dropdown. `onOpen` is a special reserved function that will automatically run each time you open (or refresh the page) the CRM spreadsheet, but we have to trigger it manually the first time. To do so, click the "play" button:

![run-onopen](/Graphics/run-onopen.PNG)

Now you'll be prompted to give the App Scrip project access to Google Account, which it needs in order to work. While it looks a little intimidating, remember that this is, ultimately, your code running in your spreadsheet, inside your account, so it shouldn't be cause for worry.

![demo crm auth required](/Graphics/demo%20crm%20auth%20required.png)

Click continue when prompted to being the authorization process, then

![demo crm authflow first](/Graphics/demo%20crm%20authflow%20first.png)

choose the account (if you have more than one) that has the Demo CRM stored on its Google Drive. You'll probably see a warning like

![demo crm authflow see more](/Graphics/demo%20crm%20authflow%20see%20more.png)

which seems to stop you from proceeding, but click 'see more' at the bottom, and you'll get

![demo crm authflow proceed](/Graphics/demo%20crm%20authflow%20proceed.png)

the option to proceed. Which will lead you to the final step, 

![demo crm authflow final](/Graphics/demo%20crm%20authflow%20final.png)

explicitly allowing your App Script project to do what you asked it to do!

Once you give the script permission to run, you should see a few things happen. First, a new menu option (`Utilities`) will appear, with options to `Edit Settings` and `Show Hidden Sheets`.

![utilities menu](/Graphics/utilities-menu.png)

Next, you'll be prompted to enter some initial settings: your name and the time zone.

<image>?

As the page is updated to reflect our new user settings, you'll notice that a number of tabs that were initially visible along the bottom of the screen will disappear.

Don't worry, they're not gone, just hiding! We hide these special sheets containing data and templates because editing them directly can change how the CRM works, or even break it. We can always unhide them via the `Utilities` menu when it's time to make changes to how the CRM works.

<final image>

Congrats, you're all set up!

Unfortunately, with no data, it's pretty empty right now. Try clicking the `Add Person` (or Org, or History) buttons, and enter some information, to get a feel for how it works. 

I don't think Demo CRM has enough functionality to be useful as it stands, but I hope it'll serve as an interesting example project as you get started exploring the wonderful world of App Script and GSuite extensions. I do intend to keep developing Demo CRM, eventually, so if you'd like get notified when I make changes, sign up for Github and watch the [repo](https://github.com/selllikesybok/SC-Atlanta-2018).

Notice a bug, want to suggest the next feature, etc? Pop open a [new Issue](/issues/new) and let me know!
