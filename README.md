# JS-verkefni3  
**1. Útskýrðu hvernig objectar tengjast í JavaScript.**  
Allir objectar sem maður býr til eiga sama "pabbann" og "afann". Objectinn erfir aðferðir frá Object.prototype, Object.prototype erfir aðferðir frá null. Ef maður býr t.d. til array erfir array aðferðir frá Array.prototype sem erfir aðferðir frá Object.prototype. Það sama á við föll og Number.  

**2. Útskýrðu kóðann línu fyrir línu:**  
Býr til fallið Book, this.isbn til að Book objectinn geti sett gildið inn í isbn.
Setur fall inn í Book með prototype aðferðinni.
Býr til nýjann object og notar Book fallið sem smið.  

**3. Kóði a:**  
```javascript
function Geimflaug(){
    this.speed = 10;
    this.life = 10;
};

let g1 = new Geimflaug();
let g2 = new Geimflaug();
let g3 = new Geimflaug();

g1.speed = 15;
g2.speed = 12;
g3.speed = 11;

Geimflaug.prototype.fly = function(){
    this.speed = this.speed + 1;
};

g1.setLife = function(){
    this.life = this.life + 1;
};
```  
**3. Kóði b:**  
```javascript
function Geimflaug(speed, life){
    this.speed = speed;
    this.life = life;
};

let g1 = new Geimflaug(10, 10);
let g2 = new Geimflaug(10, 10);
let g3 = new Geimflaug(10, 10);

g1.speed = 15;
g2.speed = 12;
g3.speed = 11;

Geimflaug.prototype.fly = function(speedUp) {
    this.speed += speedUp
};
g1.fly(1);
g2.fly(1);
g3.fly(1);

Geimflaug.prototype.setLife = function(lifeUp) {
    this.life += lifeUp
};

g1.setLife(1);
```  
**4. class**  
```javascript
class Geimflaug {
	constructor(speed, life) {
		this.speed = 10;
		this.life = 10;
	}
};
```
