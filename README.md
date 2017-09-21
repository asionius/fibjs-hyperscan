# hyperscan-fibjs
[hyperscan](https://github.com/01org/hyperscan) is a high-performance multiple regex matching library.

It uses hybrid automata techniques to allow simultaneous matching of large numbers (up to tens of thousands) of regular expressions and for the matching of regular expressions across block data.

This project integrate hyperscan in [fibjs](https://github.com/fibjs/fibjs), to enable developers to use hyperscan in their javascript projects.

It has a great advantage in fileds like text diming, keywords matching and so many on.

# prerequisite
You need to install libhs.so or libhs.dylib in your system or put them in your current work directory before you use fibjs-hyperscan.

# download
```
git clone https://github.com/asionius/fibjs-hyperscan.git
```
# install
```
cd fibjs-hyperscan
chmod +x fibjs-hyperscan-linux-x64-v0.14
cp ./fibjs-hyperscan-linux-x64-v0.14 /usr/local/bin/fibjs
```
# test
```
fibjs hs_test.js
```
# src code

[https://github.com/asionius/fibjs/tree/newHs](https://github.com/asionius/fibjs/tree/newHs)

# example
```
var reg = hs.compile("hello", "L");
var res = reg.scan("this is a hello world test text");
console.log(res);
/*
{
	"hello": [
		[10, 15]
	]
}
*/
```

# document
- click docs -> click manual -> click module -> click ifs -> click hyperscan