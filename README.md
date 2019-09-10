# horse-contest-vue
Project for organizing and running horse competition, with marking system; written using Vue.js framework.
It uses MongoDB as database and express with mongoose as backend. Communication with Vue app is done by using websockets.
Vue app uses its store and router modules.

## Run
Install all required node modules by running `npm install` and start application with `npm start`. That script will run application, background server and randomizer concurrently.


### Marking system
Horses are assigned a class in which they are judged. A class has its own set of judges. There are 5 categories which every judge gives his mark as a number between 0 and 20 in 0.5 step. All points are sumed and horse with biggest amount of points is a winner.
When 2 horses have the same amount of sumed points, marking system is comparing sum of 1-st category of each respective horse. When that comparition is resulting in the same amount of points 5-th category is compered like previosly, when that has the same result an independent judge is called to pick the winner.
