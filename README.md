# git_npm_bower_configs
The Helper: for use of git, npm or bower, behind proxy

This configs help you to use git, npm or bower using proxy.

- in bash,terminal,cmd,... need:
```
export http_proxy=http://_YOUR_USER_:_YOUR_PASSWORD_@_PROXY_IP_:_PROXY_PORT_/
export https_proxy=http://_YOUR_USER_:_YOUR_PASSWORD_@_PROXY_IP_:_PROXY_PORT_/
```

- in git is necessary use of:
```
git config --global http.sslverify false
```

- in npm is necessary use of:
```
npm config set proxy "http://_YOUR_USER_:_YOUR_PASSWORD_@_PROXY_IP_:_PROXY_PORT_/"
npm confit set http.proxy "http://_YOUR_USER_:_YOUR_PASSWORD_@_PROXY_IP_:_PROXY_PORT_/"
npm config set strict-ssl false
```

- in bower is necessary create file ".bowerrc"
  - for global use need create in Directory / 
  - for use home create in Directory ~
  - for use in local folder create inside
```
{
  "registry":"http://bower.herokuapp.com",
  "proxy":"http://_YOUR_USER_:_YOUR_PASSWORD_@_PROXY_IP_:_PROXY_PORT_",
  "https-proxy":"http://_YOUR_USER_:_YOUR_PASSWORD_@_PROXY_IP_:_PROXY_PORT_",
  "strict-ssl":false
}
```

now is possible:
```
npm install _ANY_PACK_

git clone _ANY_PACK_

bower install _ANY_PACK_
```
