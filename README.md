#MongoNotebookManager


IPython Notebook Manager in MongoDB

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