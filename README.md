## How To

### Create systemd service
  - Create a new service file
  ```
  sudo nano /etc/systemd/system/testserverapp.service
  ```

  - Put configuration as below and save
  ```
  [Unit]
  description=Testserver
  After=network.target
  [Service]
  Type=simple
  WorkingDirectory=/home/ubuntu/app/testserver
  ExecStart=/home/ubuntu/app/testserver/run.sh
  Restart=on-failure
  RestartSec=5
  [Install]
  WantedBy=multi-user.target
  ```

  - Activate and test the service
  ```
  sudo systemctl daemon-reload
  sudo systemctl enable testserverapp
  sudo systemctl start testserverapp
  sudo systemctl stop testserverapp
  sudo systemctl restart testserverapp
  systemctl -l status testserverapp.service
  journalctl -u testserverapp.service
  ```

### Zip/Unzip folder in ubuntu using command line
  - Install Zip/Unzip tools
  ```
  sudo apt install zip unzip
  ```
  - Run following commands to zip
  ```
  zip -r filename.zip /path/to/folder
  unzip master.zip
  unzip -d /path/to/folder master.zip
  ```

### [Unexpected await inside a loop. (no-await-in-loop)](https://stackoverflow.com/questions/48957022/unexpected-await-inside-a-loop-no-await-in-loop)

### [Connecting to AWS EC2 instance through remote desktop](https://stackoverflow.com/questions/50100360/connecting-to-aws-ec2-instance-through-remote-desktop)

### [JWT refresh token workflow](https://stackoverflow.com/questions/27726066/jwt-refresh-token-flow)

### [Add username and Personal Access Token to git remote origin](https://stackoverflow.com/questions/10116373/git-push-error-repository-not-found)

### [How to run index.html in localhost](https://stackoverflow.com/questions/38497334/how-to-run-html-file-on-localhost)

### [How to implement caching in Node.js using Redis](https://www.digitalocean.com/community/tutorials/how-to-implement-caching-in-node-js-using-redis)

### [Reset local repository branch to be just like remote repository HEAD](https://stackoverflow.com/questions/1628088/reset-local-repository-branch-to-be-just-like-remote-repository-head)

### [Postgres password authentication fails](https://askubuntu.com/questions/413585/postgres-password-authentication-fails)

## Tools and services
  ### Tile servers
  | Name | Database | Dynamic Data | Filtering | Backend Clustering |
  | --- | --- | --- | --- | --- |
  | [Tileserver GL](https://github.com/maptiler/tileserver-gl) | Sqlite | No | No | No |
  | [Martin](https://github.com/maplibre/martin/tree/v0.6#readme) | Postgres/PostGIS | Yes | Yes | No |
  | [Clusterbuster](https://github.com/chargetrip/clusterbuster) | Postgres/PostGIS | Yes | Yes | Yes |

## Interviews
- [Deep Cloning in Javascript](https://dev.to/builderio/deep-cloning-objects-in-javascript-the-modern-way-17kf)
- [Javascript Interview Questions](https://dev.to/onlydevs_/5-github-repositories-to-prepare-for-javascript-interviews-20lk)
- [Node.js beginner to senior course](https://github.com/flashohq/open-source-nodejs-courses)
