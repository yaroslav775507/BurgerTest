
![Снимок экрана 2023-06-22 в 21.07.55.png](..%2F..%2F..%2FDesktop%2F%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202023-06-22%20%D0%B2%2021.07.55.png)![Снимок экрана 2023-06-22 в 21.12.15.png](..%2F..%2F..%2F..%2F..%2Fvar%2Ffolders%2F9c%2Fp_z6c2m52pn71250yf4hc6500000gn%2FT%2FTemporaryItems%2FNSIRD_screencaptureui_WtooyW%2F%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA%20%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0%202023-06-22%20%D0%B2%2021.12.15.png)
let prices = document.getElementsByClassName("prod-item-price");
document.getElementById("change-currency").onclick = function (e) {
let currentCurrency = e.target.innerText;
let newCurrency = "$";
let coefficient = 1;
if(currentCurrency === "$" ){
newCurrency = "P";
coefficient = 80;
}else if(currentCurrency === "P" ){
newCurrency = "BYN";
coefficient = 3;
}else if (currentCurrency === 'BYN') {
newCurrency = '€';
coefficient = 0.9;
} else if (currentCurrency === '€') {
newCurrency = '¥';
coefficient = 6.9;
}
e.target.innerText = newCurrency;
for (let i = 0; i < prices.length; i++) {
prices[i].innerText = +(prices[i].getAttribute("data-base-price") * coefficient).toFixed(1) + " " + newCurrency;
}
}


Подключен script, который меняет валюту
А так же дает подсказки по незаполненым полям