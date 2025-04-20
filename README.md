# Tugas1
https://studio.firebase.google.com/tugas1-55802171

#Flask sederhanah
import os

from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
  """Example Hello World route."""
  name = os.environ.get("NAME", "World")
  return f"Hello {name}!"

if __name__ == "__main__":
  app.run(debug=True, host="0.0.0.0", port=int(os.environ.get("PORT", 3000)))


#Mengatur halaman untuk appnya
  from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello, Flask!"
    
@app.route('/about')
def about():
    return render_template('about.html')

if __name__ == "__main__":
    app.run(debug=False)


#Routing Dinamis
    @app.route('/nama/<string:nama>')
def getnama(nama):
    return "nama anda adalah {fawaz}".format(nama)


#Variabel dalam Routing
from flask import Flask

app = Flask(__name__)

@app.route('/user/<name>')  # Variabel name diambil dari URL
def user(fawaz):
    return f"Hello, {fawaz}!"

if __name__ == '__main__':
    app.run(debug=True)
