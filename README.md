from flask import Flask
app = Flask(__name__)

@app.route('/')

def home():

    return "We have successfully migrated the application from VM to AWS cloud", 200


if __name__ == '__main__':
    app.run(host='127.0.0.1', port=5000)
