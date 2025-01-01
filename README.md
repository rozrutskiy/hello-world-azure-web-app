    Set Up Your Local Environment
python -m venv venv

    Activate VE
source venv/bin/activate

    Verify the virtual environment is active:
which python
    
    Install all what is needed for the project:
pip install -r requirements.txt

    verify flask got installed from requirements.txt
pip freeze

    start an app
python flaskblog.py

    If you need to interact with the database (e.g., add, edit, or query data), use the flask shell command:

    First, set the FLASK_APP environment variable:
export FLASK_APP=flaskblog

    after that you can Start the Flask shell:
flask shell

    Inside the shell:
from flaskblog import db, User, Post
user_1 = User(username='andrii', email='a@demo.com', password='password')
db.session.add(user_1)
db.session.commit()
