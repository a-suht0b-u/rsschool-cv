# Suhrob Abdunabiev

*Junior software engnieer and frontend developer*

[![Personal photo](./static/img/personal_photo.jpg "Personal photo")](./static/img/personal_photo.jpg "Personal photo")

## Personal info

**First name** : *Sukhrob*

**Second name**: *Abdunabiev*

**Date of birth** : *12.06.2000*

**Marital status** : *single*


|  Contacts | Type  | Value  |
| :------------: | :------------: | :------------: |
|1| Email | a.suhrob.u@gmail.com |
|2| Telephone number  | +998 93 5877855  |
|3| Telegram  | @asuhr0b  |
|4| Whatsup  | +998 93 5877855  |
|5| Discord (rs-school) |  Suhrob (@a-suht0b-u) |
|6| Wechat | a_suhrob_u|
|7| Codeforces | dewars |

### Profile

>Hello, my name is Sukhrob Abdunabiyev, today I am a student at the school of "software engineering" at the University of China. I am interested from school in various aspects of programming, such as robotics (Arduino), writing algorithms (C++) and creating applications (js[React,Node], C++) and others. In order to always meet the advanced standard and requirements, I am not delving into modern technology and new aspects of modern programming languages, as I consider it necessary to become a competitive specialist. Currently, I work as a frontend developer in a marketing company (create different information sites for customers, such as landing pages, etc.).I can also say that I am highly motivated and deformed.
***P.S. I am ready to do my utmost to pass this selection and become your partner.***

## Education Background

### Education

| №  | Name  | From | To  | Major  | Country |
| :------------: | :------------: | :------------: | :------------: | :------------: | :------------: |
| 1 | Huazhong university of science and technology  | 2019  | now  | Software engineering | China  |
| 2 | Professional Collage of Inforamtion Technologies of Tashkent | 2016 | 2019 | Computer engineering | Tashkent |

### Language skills

| №  | Language  | Level  | Skills  | Details  |
| :------------: | :------------: | :------------: | :------------: | :------------: |
| 1  | Uzbek  | Native  | fluency in all aspects of the language  | use it for communication and study, especially school  |
| 2  | Russian  | Native  | fluency in all aspects of the language  | use it for communication and study, especially school  |
| 3  | English  |  B1-B2  | fluency in reading, listening, writing  | use it for communication and study up to now  |
| 4 | Chinese |  HSK 4-5 | very good command | mainly use it for communication and study in China | 

## Professional skills

### Programming languages

| №  | Language  | Level of native (standardized/built-in) aspects | Experience | Use for | Frameworks   |
| :------------: | :------------: | :------------: | :------------: | :------------: | :------------: |
| 1  | js  | good  | 1.5+ years  | web, algorithms, apps |1.React(strong-mid)  2.Node.js+Express.js (strong-basic) 3.React(strong-mid)  |
| 2  |  C++ | middle  | 1.5+ years  | algorithms  | Qt (basic)  |
| 3 | Python  | middle  | 1.5 years  |  allgorithms | -  |
| 4 | C#  | middle  | 1 year  | study OOP  |  1.LINQ 2.Entity Framework |
| 5 | Java  | basic  | 1 year  | study OOP  | - |

### Front-end technologies

| №  | Technology  | Level  | Details  |
| :------------: | :------------: | :------------: | :------------: |
| 1 | HTML5  | good  | Mainly use all modern html tags and concepts  |
| 2 | CSS3  | good  | Grid, Flex, modern CSS UI etc   |

### Database Skills

| №  | Technology  | Level | Use with  | Details  |
| :------------: | :------------: | :------------: | :------------: | :------------: |
| 1 |  MobgoDB  |  strong-basic - middle |  Node.js(Express.js)  |  Also basicly know Mongoose|
| 2 |  SQL (Oracle)  |  strong-basic |  -  |  Query, Join, Union etc  |

### Technical Skills

- Rich expirience of using PC
- Using OS : Windows, Linux (Ubuntu)
- Arduino
- Assembly (basics)
- Algorithms and Data Structure
- OOP patterns (GoF)
- Git + GitHub
- **IDE** : *Visual Studio, Visual Studio Code*

### Example of my codes

**1. Javascript** *(Node.js)* - solving a competive task in Codeforces platform

```javascript
Number.prototype.toInt = function () {
	return parseInt(this);
};
String.prototype.toNumber = function () {
	return +this;
};
String.prototype.clone = function () {
	return this.slice();
};
Array.prototype.unique = function () {
	return [...new Set(this)];
}

const readline = require('readline');

const rl = readline.createInterface({
	input: process.stdin,
	output: process.stdout,
});

class Input {

	constructor() {
		this._lineIndex = 0
		this._inputsBuffer = []
	}

	get _currentLine() {
		return this._lineIndex++;
	}

	buffer(value) {
		this._inputsBuffer.push(value);
	}

	readLine() {
		return this._inputsBuffer[this._currentLine];
	}

	readNumber() {
		return this.readLine().toNumber();
	}

	readArray() {
		return this.readLine().split(' ');
	}
 
	readIntArray() {
		return this.readArray().map(item => parseInt(item));
	}

}

const io = new Input();

rl.on('line', (input) => {
	io.buffer(input);
});

rl.on('close', () => {
	// const lines = require('fs').readFileSync('test.in', 'utf8').split('\n')
	let [len, maxDigit] = io.readIntArray();
	let ans = 0;
 
	while (len--) {
		const sufficientDigits = io.readLine()
			.split('')
			.unique()
			.sort()
			.slice(0, maxDigit + 1);
		ans += sufficientDigits
			.reduce((total, digit, index) => total & (digit == index),
				sufficientDigits.length === maxDigit + 1);
	}

	console.log(ans);
});
```

**2. C++** -  solving a competive task in Codeforces platform

```cpp
#include <bits/stdc++.h>
#define CPP_IO_BOOSTER	    ios_base::sync_with_stdio(0); cin.tie(0); cout.tie(0)

using namespace std;

size_t count_set_bits(size_t num) 
{
    size_t set_bits{};
    while (num) {
        set_bits += num & 1;
        num >>= 1;
    }
    return set_bits;
}

inline void solve()
{
    size_t soldiers_typies,
			  players_number,
	          acceptable_bit_diff,
	          friends{};
    cin >> soldiers_typies >> players_number >> acceptable_bit_diff;

	vector<size_t> armies(players_number + 1);

    ranges::for_each(armies, [](auto& army) {cin >> army; });

    for_each(armies.begin(), prev(armies.end()), [&friends, &armies,&acceptable_bit_diff](const auto& army){
            friends += (count_set_bits(army ^ armies.back()) <= acceptable_bit_diff);
        }
    );

    cout << friends;
}
int main()
{
	CPP_IO_BOOSTER;

    int test_cases;
    cin >> test_cases;
    while (test_cases--)
         solve();
}
```

**3. Python**

```python
class CircleLine:
    def __init__(self,start,destination,distances):
        self.start= min(start,destination)-1
        self.destination= max(start,destination)-1
        self.distances=distances
    def Ans(self):
        temp=sum(self.distances[self.start:self.destination])
        return min(temp,sum(self.distances)-temp)
    def __str__(self):
        return '{}'.format(self.Ans())

input()
distances=list(map(int,input().split()))
p1,p2=map(int,input().split())
print(CircleLine(p1,p2,distances))
```

*The other real examples of my code you can find on next resources : &darr;*

1. [Compettive Programming (Algorithms) [My Codeforces account]](https://codeforces.com/submissions/Dewars/page/7 "Compettive Programming (Algorithms) [My Codeforces account]")
2. [My GitHub account]( https://github.com/a-suht0b-u "My GitHub account") [My Projects] :
	- [React](https://github.com/a-suht0b-u/ReactApp "React")
	- [CSS/HTML](https://github.com/a-suht0b-u/CSS "CSS/HTML")
	- [Python *(Django)*](https://github.com/a-suht0b-u/Django-News-blog "Python *(Django)*")


### Additional Trainings

1. [Udemy](https://www.udemy.com "Udemy")
	- JavaScript Courses:
		- [JS ](https://www.udemy.com/course/the-complete-javascript-course/ "JS ")
		- [React](https://www.udemy.com/course/react-the-complete-guide-incl-redux/ "React")
		- [Node.js + Express.js](https://www.udemy.com/course/nodejs-express-mongodb-bootcamp/ "Node.js + Express.js")
	- [HTML5 & CSS3 & SASS](https://www.udemy.com/course/advanced-css-and-sass/ "HTML5 & CSS3 & SASS")
	- Databases:
		- [MongoDB](https://www.udemy.com/course/mongodb-the-complete-developers-guide/ "MongoDB")
		- [Oracle SQL](https://www.udemy.com/course/sql-oracle-certification/ "Oracle SQL")
2. OTUS:
	- C++
3. CyberBionic Systematics:
	- [C#](https://edu.cbsystematics.com/ru/courses-and-prices#FF7F8424-653B-401B-9888-902CBEE45F4A "C#")
