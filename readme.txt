# python and flask:
virtual invironment python -m venv venv
to activate /venv/script/activate/
dependencies for :
    pip install flask flask-sqlalchemy flask-cors
        --flask-cors to deals with flusk errors
        --flask-sqlalchemy for ORMS-python to manage data from database without using sql code


#to run 
    set FLASK_APP=app.py
    set FLASK_ENV=development
    flask run
    flask run --reload


app = Flask(__name__)
This line creates your web application instance.
Think of app as the main engine of your backend.__name__ is a special Python variable
 that tells Flask where your project files, templates, 
 and folders live so it can configure itself properly.
Once this line runs, you can start creating paths (routes) for your application, 
like @app.route('/api/bank')


CORS(app)This line enables Cross-Origin Resource Sharing (CORS) for your entire app. 
It is a critical layer of security for modern web development.

#adding configuration and db:
    app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///friends.db'
    app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False
       --this is to create database and to track modification this sonfiguration are used

    db = SQLAlchemy(app)----variable 


     'sqlite:///friends.db' this line up there is your db nane friend.db


     if __name__ == "__main__":
       app.run(debug=True) to not run while importing in other



# TO CREATE FRONTEND
npm create vite@latest .


#In the deployment 
cd forntend
npm run build

-> then 
 import os
 --frontend_folder=os.path.join(os.getcwd(),"..","frontend","dist")
 or 
 frontend_folder=os.path.join(os.getcwd(),"..","frontend")
dist_folder=os.path.join(frontend_folder,"dist")