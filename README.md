<!DOCTYPE html><html lang="en"><head><meta charset="UTF-8"><meta name="viewport"
content="width=device-width,initial-scale=1">

<title>Ramesh Fancy Store

</title><style>

*{

margin:0;

padding:0;

box-sizing:border-box;

font-family:Arial;

}

body{

background:#f5f5f5;

}

header{

background:#111;

color:white;

padding:50px;

text-align:center;

}

.hero{

padding:20px;

text-align:center;

background:white;

}

.grid{

display:grid;

grid-template-columns:
repeat(
auto-fit,
minmax(
240px,
1fr
)

);

gap:20px;

padding:25px;

}

.card{

background:white;

border-radius:18px;

overflow:hidden;

box-shadow:
0 5px 15px rgba(
0,
0,
0,
.1
);

}

.card img{

width:100%;

height:320px;

object-fit:cover;

}

.card h3{

padding:10px;

}

.price{

padding:0 10px;

color:#ff0055;

font-weight:bold;

}

.buy{

margin:15px;

width:
calc(
100% - 30px
);

padding:12px;

background:black;

color:white;

border:none;

border-radius:30px;

}

#order{

display:none;

background:white;

margin:25px;

padding:25px;

border-radius:20px;

}

input{

width:100%;

padding:14px;

margin-top:12px;

}

.send{

margin-top:15px;

width:100%;

padding:14px;

background:black;

color:white;

border:none;

}

</style></head><body><header><h1>Ramesh Fancy Store

</h1><p>📍 Rapti–1 Bhalubang

</p><p>🕗 Open 8AM

</p><p>🌙 Close 9PM

</p><p>🚚 Delivery Available

</p><p>📞 9763470784

</p></header><div
class="hero"><h2>Men & Women Collection

</h2></div><div
id="shop"><div
class="grid"
id="products"></div></div><div
id="order"><h2>Place Order

</h2><br><p
id="cloth"></p><p
id="price"></p><input
id="name"
placeholder="Your Name">

<input
id="address"
placeholder="Address">

<input
id="phone"
placeholder="Phone Number">

<button
class="send"
onclick="sendOrder()">

Send Order 🚚

</button></div><script>

const clothes=[

["Men Shirt",1200],
["Men Hoodie",2500],
["Men Jacket",3500],
["Men Jeans",2200],
["Men T Shirt",900],

["Women Kurti",1800],
["Women Dress",3200],
["Women Jacket",3400],
["Women Top",1300],
["Women Saree",4500],

["Men Formal",2800],
["Women Fancy",3000],
["Men Cargo",2400],
["Women Hoodie",2600],
["Men Coat",6000],

["Women Kurtha",1900],
["Men Polo",1400],
["Women Jeans",2100],
["Men Summer Set",1800],
["Women Premium Set",5200]

];

let selected="";
let selectedPrice="";

let html="";

clothes.forEach((c,i)=>{

html+=`

<div
class="card">

<img
src=
"https://picsum.photos/500/650?random=${i}"

>

<h3>

${c[0]}

</h3>

<div
class="price">

Rs ${c[1]}

</div>

<button

class="buy"

onclick=
"buy(
'${c[0]}',
'${c[1]}'
)"

>

Buy Now

</button>

</div>

`;

});

products.innerHTML=html;

function buy(a,b){

selected=a;

selectedPrice=b;

shop.style.display=
"none";

order.style.display=
"block";

cloth.innerText=
"Item: "+a;

price.innerText=
"Price: Rs "+b;

window.scrollTo(
0,
0
);

}

function sendOrder(){

if(

!name.value||

!address.value||

!phone.value

){

alert(

"Fill all details"

);

return;

}

const msg=

`🛍️ NEW ORDER

Store:
Ramesh Fancy Store

Item:
${selected}

Price:
Rs ${selectedPrice}

Name:
${name.value}

Address:
${address.value}

Phone:
${phone.value}`;

window.location.href=

`https://wa.me/9779763470784?text=${encodeURIComponent(msg)}`;

}

</script></body></html>
