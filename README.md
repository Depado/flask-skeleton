# Flask-Skeleton
----------
### Main Goal of the Project ###
The main goal of this project is to generate easily a skeleton for a simple or more complex Flask application.

### Arguments and Usage ###
[![asciicast](https://asciinema.org/a/10051.png)](https://asciinema.org/a/10051)

The simpler way for now to use this script is to add the path as an alias in your .bashrc / fish.config.
Exemple :

    alias flaskeleton="python /full/path/to/script/flask_project.py"
    
And then use it by just calling `flaskeleton`

#### Arguments ####

 - --virtualenv or -v : 
 Generate a virtual environment to isolate your libs from the system libs. It also permits to install dependencies as non-root user. The dependencies for the project will be installed with the virtualenv so it can work out of the box.
 - --bower [args] or -b [args] :
 Will install static dependencies in the flask static directory of the generated project using bower. Note that you need to have it installed on your system for this option to work. Otherwise the generation won't even begin. (If you don't have bower, ignore this option).
 - --database or -d :
 Will generate a project with a database using the plugin Flask-SQLAlchemy. This generated project comes with a predefined User model so you can see how a model is declared. The database will be an sqlite one and you have to create the database once your models are defined. This option also installs the Flask-Migrate plugin so you can run your own migrations.
 - --no-debug or -n :
 Disables the DEBUG mode. Note that in production it may be a good thing to keep this option to true as Green Unicorn or UWSGI uses the errors generated by the debug mode to create the log files.
 - --git or -g :
 Initialise an empty git repository in the folder and copy a sample gitignore file so you don't add some things like all your .pyc to your project by mistake.
 

