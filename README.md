# nodered-heroku
A wrapper for deploying [Node-RED](http://nodered.org) into the [Heroku](https://www.heroku.com).
* DEMO: Flow Editor - [https://nodered-heroku.herokuapp.com/editor](https://nodered-heroku.herokuapp.com/editor)
* DEMO: Dashboard UI - [https://nodered-heroku.herokuapp.com](https://nodered-heroku.herokuapp.com)


# Warning: You will lost all saved flows every time heroku restart!
* SOLUTION: To overcome this, on Editor, after finish with your design and deployed, you need to Export 'all flows' as "flows.json" file, and push your "flows.json" to your github, linked to your heroku. Detail on step 4 and 5.

# 1. Deploying Node-RED into Heroku  [![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/Sevenmojoe/nodered-heroku)

# 2. Set Username and Password for your Flow Editor
* NODE_RED_USERNAME - replace this with Username for Flow Editor
* NODE_RED_PASSWORD - replace this with Password for Flow Editor

# 3. Access your Node-Red
* Flow Editor - [nodered-on-cloud.herokuapp.com/editor](https://nodered-on-cloud.herokuapp.com/editor)
* Dashboard UI - [nodered-on-cloud.herokuapp.com](https://nodered-on-cloud.herokuapp.com)

# 4. Export all flows as "flows.json" and "flows_cred.json" files AFTER you create your flow and deploy it
* flows.json - In Editor, click hamburger icon (top right), click Export, choose tab "All flows", then Download.
* flows-cred.json - Browse the /app folder, e.g., with this [flow](https://flows.nodered.org/flow/44bc7ad491aacb4253dd8a5f757b5407) or the [modified version](utils/file-explorer-flow.json), and download.

# 5. Fork this repo, Set your github as deploy source on Heroku setting, and enable Automatic Deployment
* Push downloaded "flows.json" file to your repo on github.
* Every time "flows.json" pushed to your repo, Heroku will rebuild node-red with updated "flows.json".
* So your node-red will always have latest pushed "flows.json" when Heroku dynos restarted.

# *Some included nodes
* Dashboard UI - node-red-dashboard
* MQTT - node-red-contrib-aedes
* Blynk Cloud - node-red-contrib-blynk-ws
* Email - node-red-node-email
* Telegram - node-red-contrib-telegrambot-home
* InfluxDB, MongoDB, Modbus, OPC UA, Netatmo, PostgresSQL, Wordmap, etc. 
