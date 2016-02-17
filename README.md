# nodejs

http://stackoverflow.com/

https://www.npmjs.com/

nodejs 官网：https://nodejs.org/en/

nodejs中的module.exports  与exports.xx 深入理解：http://www.cnblogs.com/pigtail/archive/2013/01/14/2859555.html

nodejs的版本不同，代码的语法可能不一样 如：nodejs 4.3.0  与v0.12.0
一般情况下高版本的会兼容低版本的语法
//4.3.0 

const http = require('http');
http.createServer( (request, response) => {
  response.writeHead(200, {'Content-Type': 'text/plain'});
  response.end('Hello World\n');
}).listen(8124);
console.log('Server running at http://127.0.0.1:8124/');

//v0.12.0

var http=require('http');
http.createServer(function(req,res){
	res.writeHead(200,{'Content-Type':'text/plain'});
	res.end('Hello world\n');
}).listen(1337,'127.0.0.1');
console.log('Server running at http://127.0.0.1:1377/');
