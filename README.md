#   Taiyuan City Dashboard 桃園城市儀表板
<img src='src/assets/images/dashboard_intersection.png'> 
<img src='src/assets/images/dashboard_zhongbei_intersection.png'> 
<img src='src/assets/images/map01.png'> 
<img src='src/assets/images/map02.png'> 
<img src='src/assets/images/map03.png'> 
<img src='src/assets/images/map04.png'> 
<img src='src/assets/images/component_detail.png'> 



## Quick Start

### Docker

1. Install [Docker](https://www.docker.com/products/docker-desktop/) on your computer and start running it.
2. Fork this repository then clone the project to your computer. Execute `pwd` (mac) or `cd` in the repository terminal to get the complete path.
3. Execute the following command in the system terminal and replace "<repository path>" with the path you got in step 2.

```bash
docker run -v <repository path>:/opt/Taipei-City-Dashboard-FE -p 80:80 -it node:18.18.1-alpine3.18  sh
```

4. Execute the following commands to enter the project folder and install packages.

```bash
cd /opt/Taipei-City-Dashboard-FE
npm install
```

5. You should now be able to locally host this project by executing `npm run dev` in the respository terminal.
6. Refer to the [Docs](https://tuic.gov.taipei/documentation/front-end/project-setup) to complete further configurations.

### Local Environment

1. Download [Node.js](https://nodejs.org/en) on your computer.
2. Fork this repository then clone the project to your computer.
3. Execute `npm install` in the respository terminal
4. You should now be able to locally host this project by executing `npm run dev` in the respository terminal.
5. Refer to the [Docs](https://tuic.gov.taipei/documentation/front-end/project-setup) to complete further configurations.

## Documentation
Develop Taoyuan City Dashboard based on Taipei City Dashboard.
Check out the complete documentation for Taipei City Dashboard FE [here](https://tuic.gov.taipei/documentation).
