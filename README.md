#MongoNotebookManager


IPython Notebook Manager in MongoDB

##Setting up

First, run

    pip install MongoNotebookManager

Then, when you start ipython notebook, make sure you have the following config settings in place. This module will save your notebooks and checkpoints to mongodb, and supports an unlimited number of checkpoints.

###required

    NotebookApp.notebook_manager_class=mongo_notebook_manager.MongoNotebookManager

###optional

Below are the arguments, with their default values

####mongo_uri

    MongoNotebookManager.mongo_uri='mongodb://localhost:27017/'

####replica_set

    MongoNotebookManager.replica_set=''

####database_name

    MongoNotebookManager.database_name='ipython'

####notebook_collection

    MongoNotebookManager.notebook_collection='notebooks'

####checkpoint_collection

    MongoNotebookManager.checkpoint_collection='checkpoints'

####checkpoints_history

    MongoNotebookManager.checkpoints_history=False

##Why did I build this?

I was setting up IPython Notebook on heroku, and ran into the problem where heroku will remove the extra files after a while. Having used mongodb quite thoroughly before, and knowing the existence of the free mongodb host (up to 500mb, which I believe is more than enough for most users of IPython Notebook), mongolab, I decided to write a module that will enable persistence of the notebooks on heroku, hence this plugin.

##Bugs?

This is still in Alpha stage, although most of the basic features are working. If you do find any bugs, please report issues to the [repo on Github](https://github.com/laurenceputra/mongo_notebook_manager/issues).

##Features?

If there are additional features that you are looking for, please create an issue over at our [repo on Github](https://github.com/laurenceputra/mongo_notebook_manager/issues), and we'll prioritize and get working on it.

##Pull requests?

If you wish to make things better, or fix one of the issues(bug/feature), please submit a pull request. However, please follow the [AngularJS commit message guideline](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#commit) for your commit messages.
