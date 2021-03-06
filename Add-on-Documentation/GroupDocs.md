#GroupDocs

GroupDocs is a one-stop-shop for your document management requirements.

## Adding GroupDocs

GroupDocs can be added by executing the command addon.add:

    $ ironapp APP_NAME/DEPLOYMENT addon.add groupdocs.PLAN_NAME

## Removing GroupDocs

Similarly, the Add-on can be removed from the deployment easily using addon.remove:

    $ ironapp APP_NAME/DEPLOYMENT addon.remove groupdocs.PLAN_NAME

## Sample GroupDocs app

If you just want to try GroupDocs out but haven't got any app running yet, you can clone the GroupDocs sample app:

	$ git clone git://github.com/groupdocs/groupdocs-cloudcontrol-examples-for-python.git

Store the app on Git:

	$ cd groupdocs-cloudcontrol-examples-for-python
    $ git init
    $ git add .
    $ git commit -m "init"

Create your app on the Python CloudKilat stack:

    $ ironapp APP_NAME create python

Push and deploy the code:

    $ ironapp APP_NAME push
	$ ironapp APP_NAME deploy

This sample app is also running live on CloudKilat. To view and try, please open [http://groupdocspython.cloudcontrolapp.com/](http://groupdocspython.cloudcontrolapp.com/).
