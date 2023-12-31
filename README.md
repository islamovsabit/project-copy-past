# Class Number

## 1 Method
```js
function numberSum(N) {
    var total = 0;
    for (var i = 1; i <= N; i++) {
        total += i;
    }
    return total;
}
console.log(numberSum(100));

// answer 5050
```
## 2 Method
```js
var total = 0;
for (var i = 1; i <= 100; i++) {
    total += i;
}
console.log(total);

// answer 5050
```

## 3 Method
```js
const numSum = (n) => n * (n + 1) / 2;
console.log(numSum(100));

// answer 5050
```

## 4 Method
```js
var sum = 0;
for (var i = 1; i <= 100; i += 2) {
    sum += i;
}
console.log(sum);

// answer 2500
```

## 5 Method
```js
function sumOddEven(n) {
    const floor = Math.floor(n / 2);
    const ceil = Math.ceil(n / 2);
    return [ceil * ceil, floor * (1 + floor)];
}
console.log(sumOddEven(100)[1], sumOddEven(100)[0])

// answer 2550 2500
```

## 6 Method
```js
let even_sum = 0;
let odd_sum = 0;
for (let i = 0; i <= 100; i++) {
    if (i % 2 == 0)
        even_sum += i;
    else
        odd_sum += i;
}
console.log(even_sum, odd_sum)

// answer 2550 2500
```

## 7 Method
```js
m = [0, 0]; for (i = 0; i < 101; i++) m[i % 2] += i; console.log(m[0], m[1]);

// answer 2550 2500
```

## 8 Method
```js
let maz = 0, kaz = 0;
for (let i = 0; i <= 100; i++) if (i % 2 == 0) maz += i; else kaz += i; console.log(maz, kaz);

// answer 2550 2500
```

## 9 Method
```js
let maz = 0, kaz = 0;
function learnJavaScript(f) {
    let count = 0
    while (count < f) {
        count + ' '
        count++
    }
    return count * (count + 1) / 2;
}
console.log(learnJavaScript(100));

// answer 5050
```
# Class Material ui

## 1 Method

```html
<Button
    style={{
        borderRadius: 35,
        backgroundColor: "#21b6ae",
        padding: "18px 36px",
        fontSize: "18px"
    }}
    variant="contained"
    >
    Submit
</Button>
```

# Time Medhod

## 1 Medhod
```js
let number = 0;

function updateClock() {
    const hoursElement = document.getElementById('hrs');
    const minutesElement = document.getElementById('min');
    const secondsElement = document.getElementById('sec');
    
    const update = () => {
        const hours = String(Math.floor(number / 3600)).padStart(2, '0');
        const minutes = String(Math.floor((number % 3600) / 60)).padStart(2, '0');
        const seconds = String(number % 60).padStart(2, '0');
        
        hoursElement.textContent = hours;
        minutesElement.textContent = minutes;
        secondsElement.textContent = seconds;
        
        console.log(seconds);
        number++;
        
        if (number <= 60) {
            setTimeout(update, 1000);
        }
    };

    update();
}

updateClock();
```

## 2 Medhod 

```js
let number = 0;

function Time() {
    if (number <= 60) {
        const hours = String(Math.floor(number / 3600)).padStart(2, '0');
        const minutes = String(Math.floor((number % 3600) / 60)).padStart(2, '0');
        const seconds = String(number % 60).padStart(2, '0');
        
        document.getElementById('hrs').textContent = hours;
        document.getElementById('min').textContent = minutes;
        document.getElementById('sec').textContent = seconds;
        
        console.log(seconds);
        number++;
        
        if (number <= 60) {
            setTimeout(Time, 1000);
        }
    }
    return number;
}

Time();
```

## 3 Medhod
```js
function updateTime() {
    const now = new Date();
    const hours = String(now.getHours()).padStart(2, '0');
    const minutes = String(now.getMinutes()).padStart(2, '0');
    const seconds = String(now.getSeconds()).padStart(2, '0');
    
    document.getElementById('hrs').textContent = hours;
    document.getElementById('min').textContent = minutes;
    document.getElementById('sec').textContent = seconds;
}

setInterval(updateTime, 1000); // Vaqt o'zgarishini har 1 sekundda yangilash
updateTime();
```
## 4 Medhod Parallax
```js
attribute: data-speed="2.5"
function:
let img = document.querySelector(".images")

window.addEventListener("scroll", () =>{
    console.log(this.scrollY);
    let speed  = +img.getAttribute("data-speed")
    
    img.style.transform = `translateX(${scrollY * speed}px)`
})
```

## 4 Medhot Revalidate
```js
async function getData() {
    const res = await fetch('https://bilmervipapi.pythonanywhere.com/next_api/all-news/', { next: { revalidate: 3 } }, { cache: 'no-store' })
    if (!res.ok) {
        throw new Error('Failed to fetch data')
    }
    return res.json()
}

export default async function Home() {
    const data = await getData()
    console.log(data);
    return (<main>
        {data.map((item) => {
            return (
                <h2>{item.news_title}</h2>
            )
        })}
    </main>
    )
}
```

## 6 Medhot Redirect
```js
import { redirect } from 'next/navigation'
export default async function Article() {
    redirect('/')
}
```


## 7 Medhot Text Length
```js
let str = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur nemo nobis voluptatum impedit aspernatur eum laudantium temporibus, dolorem facilis '

let vowels = "";
let consonants = "";
for (let i = 0; i < str.length; i++) {
    let letter = str[i].toLowerCase();
    if ("aeiou".includes(letter)) {
        vowels += letter;
    } else if (letter >= "a" && letter <= "z") {
        consonants += letter;
    }
}

let unli = vowels.length
let undosh = consonants.length
console.log(
    unli, undosh, vowels, consonants
);
```

## 8 Medhot Category filter

### html

```html
<div>
    <button class="button-class" data-category="all">all</button>
    <button class="button-class" data-category="app">app</button>
    <button class="button-class" data-category="website">website</button>
    <button class="button-class" data-category="design">design</button>
</div>
<div id="product-container"></div>
```


### class version




```js

class Product {
    constructor(id, name, category) {
        this.id = id;
        this.name = name;
        this.category = category;
    }
    createProductElement() {
        const productElement = document.createElement('div');
        productElement.className = "bilmer";
        productElement.id = this.id;
        productElement.innerHTML = `
            <h3>${this.name}</h3>
            <p>Category: ${this.category}</p>
        `;
        return productElement;
    }
}
class ProductManager {
    constructor(products, productContainer) {
        this.products = products;
        this.productContainer = productContainer;
        this.unrepeatable = [];

        // Add click event listeners to category buttons
        categoryButtons.forEach(button => {
            button.addEventListener('click', (e) => {
                const data_category = e.target.getAttribute("data-category");
                if (data_category === "all") {
                    this.displayAllProducts();
                } else {
                    this.displayFilteredProducts(data_category);
                }
            });
        });
        this.displayAllProducts();
    }

    displayAllProducts() {
        this.clearProductContainer();
        this.unrepeatable.length = 0;
        this.products.forEach(product => {
            if (!this.unrepeatable.includes(product.id)) {
                this.unrepeatable.push(product.id);
                const productElement = product.createProductElement();
                this.productContainer.appendChild(productElement);
            }
        });
    }

    displayFilteredProducts(category) {
        this.clearProductContainer();
        this.unrepeatable.length = 0;
        const filteredProducts = this.products.filter(product => product.category === category);
        filteredProducts.forEach(product => {
            if (!this.unrepeatable.includes(product.id)) {
                this.unrepeatable.push(product.id);
                const productElement = product.createProductElement();
                this.productContainer.appendChild(productElement);
            }
        });
    }

    clearProductContainer() {
        this.productContainer.innerHTML = "";
    }
}
const products = [
    new Product(1, 'Product A', 'app'),
    new Product(2, 'Product B', 'website'),
    new Product(3, 'Product C', 'design'),
    new Product(4, 'Product D', 'design')
];
const productContainer = document.getElementById('product-container');
const categoryButtons = document.querySelectorAll('.button-class');
new ProductManager(products, productContainer);

```

### function version 

```js
const products = [
    { id: 1, name: 'Product A', category: 'app' },
    { id: 2, name: 'Product B', category: 'website' },
    { id: 3, name: 'Product C', category: 'design' },
    { id: 4, name: 'Product D', category: 'app' },
    { id: 5, name: 'Product F', category: 'design' },
    { id: 6, name: 'Product G', category: 'website' },
    { id: 7, name: 'Product H', category: 'app' },
    { id: 8, name: 'Product J', category: 'design' },
    { id: 9, name: 'Product K', category: 'app' },
    { id: 10, name: 'Product L', category: 'website' },
];
const categoryButtons = document.querySelectorAll('.button-class');
const productContainer = document.getElementById('product-container');
const unrepeatable = [];
products.forEach(product => {
    const productElement = document.createElement('div');
    productElement.className = "bilmer";
    productElement.id = product.id
    productElement.innerHTML = `
        <h3>${product.name}</h3>
        <p>Category: ${product.category}</p>
    `;
});
categoryButtons.forEach(button => {
    button.addEventListener('click', (e) => {
        const data_category = e.target.getAttribute("data-category");
        if (data_category === "all") {
            displayAllProducts();
        } else {
            displayFilteredProducts(data_category);
        }
    });
});
displayAllProducts();
async function displayAllProducts() {
    productContainer.innerHTML = "";
    unrepeatable.length = 0;
    products.forEach(product => {
        if (!unrepeatable.includes(product.id)) {
            unrepeatable.push(product.id);
            const productElement = createProductElement(product);
            productContainer.appendChild(productElement);
        }
    });
}
function displayFilteredProducts(category) {
    productContainer.innerHTML = "";
    unrepeatable.length = 0;
    const filteredProducts = products.filter(product => product.category === category);
    filteredProducts.forEach(product => {
        if (!unrepeatable.includes(product.id)) {
            unrepeatable.push(product.id);
            const productElement = createProductElement(product);
            productContainer.appendChild(productElement);
        }
    });
}
function createProductElement(product) {
    const productElement = document.createElement('div');
    productElement.className = "bilmer";
    productElement.id = product.id
    productElement.innerHTML = `
        <h3>${product.name}</h3>
        <p>Category: ${product.category}</p>
    `;
    return productElement;
}
```


## 9 Medhot Category filter

```js
async function saved_localstorage() {
    const localBasket = []
    try {
        const res = await fetch('https://portfoliobilmer.pythonanywhere.com/api/v5/portfolio-data/');
        if (!res.ok) throw new Error(`Failed to fetch data: ${res.status} ${res.statusText}`);
        const data = await res.json();
        data.forEach(e => {
            if (!localBasket.includes(e.id)) {
                localBasket.push({
                    id: e.id,
                    uploader_name: e.uploader_name,
                    portfolio_title: e.portfolio_title,
                    portfolio_text: e.portfolio_text,
                    portfolio_link: e.portfolio_link,
                    portfolio_img: e.portfolio_img,
                    portfolio_video_url: e.portfolio_video_url,
                    portfolio_data: e.portfolio_data,
                    portfolio_slug: e.portfolio_slug,
                    portfolio_category_id: e.portfolio_category,
                    portfolio_category_name: e.portfolio_category_slug.slug
                })
                localStorage.setItem(`portfolio`, JSON.stringify(localBasket))
            }
        });
    } catch (error) {
        throw new Error(`Error fetching data: ${error.message}`);
    }
}
saved_localstorage()


const btns = document.querySelectorAll('.button-class');
const container = document.getElementById('product-container');
const dataString = localStorage.getItem('portfolio');
const data = JSON.parse(dataString);

async function displayFilteredData(category) {
    container.innerHTML = "";
    data.forEach(element => {
        if (category === "all" || element.portfolio_category_name === category) {
            const truncateString = (string = '', maxLength = 50) =>
                string.length > maxLength
                    ? `${string.substring(0, maxLength)}…`
                    : string;
            const text = truncateString(element.portfolio_text, 15);
            const productElement = document.createElement('div');
            productElement.className = "bilmer";
            productElement.id = element.id;
            productElement.innerHTML = `
                <p>ID: ${element.id}</p>
                <p>Uploader Name: ${element.uploader_name}</p>
                <p>Category Name: ${element.portfolio_category_name}</p>
            `;
            container.appendChild(productElement);
        }
    });
}

btns.forEach(element => {
    element.addEventListener('click', (e) => {
        const category = e.target.getAttribute("data-category");
        displayFilteredData(category);
    });
});

async function home() {
    container.innerHTML = "";
    data.forEach(element => {
        const productElement = document.createElement('div');
        productElement.className = "bilmer";
        productElement.id = element.id;
        productElement.innerHTML = `
                <p>ID: ${element.id}</p>
                <p>Uploader Name: ${element.uploader_name}</p>
                <p>Category Name: ${element.portfolio_category_name}</p>
            `;
        container.appendChild(productElement);
    });
}
home()
```

## 10 Medhot class

```js
class MyNumber {
    constructor() {
        this.data = null;
        this.btns = document.querySelectorAll('.button-class');
        this.container = document.getElementById('product-container')
        this.get_information();
        this.click_parse();
    }

    async get_information() {
        try {
            const response = await fetch('https://portfoliobilmer.pythonanywhere.com/api/v5/portfolio-data/');
            const data = await response.json();
            this.data = data;
        } catch (error) {
            console.error('Error:', error);
        }
    }
    async click_parse() {
        this.btns.forEach(element => {
            element.addEventListener("click", (e) => {
                this.categoryName = e.target.getAttribute('data-category');
                this.html_information();
            });
        });
    }

    async html_information() {
        let count_bilmer = 0;
        if (this.data) {
            this.container.innerHTML = '';
            this.data.forEach(el => {
                if (this.categoryName === "all" || el.portfolio_category_slug.slug === this.categoryName) {
                    const bilmer = document.createElement('div');
                    bilmer.className = 'bilmer';
                    bilmer.id = 'unique-div';
                    bilmer.innerHTML = `
                        <p>${el.uploader_name}</p>
                        <p>${el.portfolio_title}</p>
                        <a href="${el.portfolio_link}">Link</a>
                        <img src="${el.portfolio_img}" />
                        <p>${el.portfolio_slug}</p>
                        <p></p>
                    `;
                    this.container.appendChild(bilmer);
                    count_bilmer++;
                }
            });
        }
    }

}
const myInstance = new MyNumber()
```


# Scroll Effect React

## Medhot 1
```js
const [scrollPosition, setScrollPosition] = useState(0);
useEffect(() => {
    const handleScroll = () => {
    setScrollPosition(window.scrollY);
};
    window.addEventListener('scroll', handleScroll);
    return () => {
        window.removeEventListener('scroll', handleScroll);
    };
}, []);
console.log(scrollPosition);

return (
    <>
        <div className='element-scroll-top'></div>
        <div className={`element-scroll-bottom ${scrollPosition > 300 ? "active" : ""}`}></div>
    </>
);
```

## Medhot 2
```js
document.addEventListener('DOMContentLoaded', function () {
    const nav_bt = document.querySelector('.nav');
    const header_bt = document.querySelector('.header');
    const header = document.getElementById('header');

    window.addEventListener('scroll', function () {
        const navHeight = nav_bt.offsetHeight; // or nav_bt.clientHeight
        const headerHeight = header_bt.offsetHeight; // or header_bt.clientHeight

        const scrollPosition = window.scrollY;
        const offset = navHeight + headerHeight;

        if (scrollPosition > offset) {
            header.style.backgroundColor = 'lightcoral';
        } else {
            header.style.backgroundColor = 'lightblue';
        }
    });
});
```
<img src="https://github.com/islamovsabit/oline-market-code/assets/147802380/b9b4bd1a-a48c-466f-85bb-eec31fd81ed1"  width="100%" />
<img src="https://github.com/islamovsabit/oline-market-code/assets/147802380/39ac37b9-d66a-4f2f-9e45-2970e5d87edb"  width="100%" />

## Medhot 3
```js

class ScrollEffect {
    constructor() {
        this.header = document.getElementById('header');
        this.header_bt = document.querySelector('.header')
        this.nav_bt = document.querySelector('.nav')
        
        this.scrollOffset = this.header_bt.offsetHeight + this.nav_bt.offsetHeight
        this.updateHeaderColor();
        window.addEventListener('scroll', () => this.updateHeaderColor());
    }
    updateHeaderColor() {
        const scrollPosition = window.scrollY;
        if (scrollPosition > this.scrollOffset) {
            this.header.style.backgroundColor = 'lightcoral';
        } else {
            this.header.style.backgroundColor = 'lightblue';
        }
    }
}

document.addEventListener('DOMContentLoaded', function () {
    const scrollEffect = new ScrollEffect();
});

```

# API fetch

## Medhot 1
```python
import requests

api_key = '855eb59e3593f561ff2838fa1f8c67500151ed54d9eec7bb9b7db46e25a5c640'
search_query = input("Search Term:")
yandex_domain = 'yandex.uz'
url = f'https://serpapi.com/search?engine=yandex_images&api_key={api_key}&text={search_query}&yandex_domain={yandex_domain}'
response = requests.get(url)
data = response.json()['images_results']
data_bt = response.json()
for i in data:
    print(i['thumbnail'])

```
run

<img src="https://github.com/islamovsabit/project-turon-university/assets/147802380/aa42955b-0822-4884-bf43-0b4884fbdc76" />

# Product Design

## Medhot 1
```html
<div id="product-list">
        <!-- Product List -->
        <div class="product" data-id="1" data-name="Product 1" data-price="20.00">
            <h2>Product 1</h2>
            <p>$20.00</p>
            <button class="button_add" onclick="addToCart(1)">Add to Cart</button>
        </div>

        <div class="product" data-id="2" data-name="Product 2" data-price="30.00">
            <h2>Product 2</h2>
            <p>$30.00</p>
            <button class="button_add" onclick="addToCart(2)">Add to Cart</button>
        </div>

        <div class="product" data-id="3" data-name="Product 3" data-price="45.00">
            <h2>Product 3</h2>
            <p>$45.00</p>
            <button class="button_add" onclick="addToCart(3)">Add to Cart</button>
        </div>

        <div class="product" data-id="4" data-name="Product 4" data-price="150.00">
            <h2>Product 4</h2>
            <p>$150.00</p>
            <button class="button_add" onclick="addToCart(4)">Add to Cart</button>
        </div>
    </div>
```

```js
<script>
        let cart = [];
        let totalSum = 0;
        window.onload = function () {
            const storedCart = JSON.parse(localStorage.getItem('cart')) || [];
            cart = storedCart;
            totalSum = parseFloat(localStorage.getItem('totalSum')) || 0;
            updateCart();
            updateButtonStates();
        };

        function isProductInCart(productId) {
            return cart.some(item => item.id === productId);
        }

        function addToCart(productId) {
            if (isProductInCart(productId)) {
                return;
            }

            const product = document.querySelector(`.product[data-id="${productId}"]`);
            const cartItem = {
                id: productId,
                name: product.dataset.name,
                price: parseFloat(product.dataset.price),
            };

            cart.push(cartItem);
            totalSum += cartItem.price;
            localStorage.setItem('cart', JSON.stringify(cart));
            localStorage.setItem('totalSum', totalSum.toString());
            updateCart();
            const addButton = product.querySelector('.button_add');
            addButton.disabled = true;
            addButton.classList.add('button_added');
        }

        function removeFromCart(index) {
            const removedItem = cart.splice(index, 1)[0];
            totalSum -= removedItem.price;
            localStorage.setItem('cart', JSON.stringify(cart));
            localStorage.setItem('totalSum', totalSum.toString());
            updateCart();
            const productId = removedItem.id;
            updateButtonStates(productId);
        }

        function updateButtonStates(productId) {
            const buttonToUpdate = document.querySelector(`.product[data-id="${productId}"] .button_add`);

            if (buttonToUpdate) {
                buttonToUpdate.disabled = false;
                buttonToUpdate.classList.remove('button_added');
            }
        }

        function updateCart() {
            const cartContainer = document.getElementById('cart');
            cartContainer.innerHTML = `<h3 class="total_bs">Total: $${totalSum.toFixed(2)}</h3>`;

            cart.forEach((item, index) => {
                const cartItem = document.createElement('div');
                cartItem.classList.add('cart-item');
                cartItem.innerHTML = `
                <h3>${item.name}</h3>
                <p>$${item.price.toFixed(2)}</p>
                <button onclick="removeFromCart(${index})">Remove</button>
            `;
                cartContainer.appendChild(cartItem);
            });
        }
    </script>
```

# Todo List

## Medhot 1
```html
<form id="todoList">
        <h2>Todo List</h2>
        <input type="text" id="taskInput" placeholder="New task...">
        <button onclick="addTask(event)">Add</button>

        <ul id="tasksList"></ul>
        <button id="removeAll" onclick="removeAllTasks()">Remove All</button>
    </form>
```
```js
function addTask(e) {
    e.preventDefault(); // Corrected typo
    var taskInput = document.getElementById("taskInput");
    var taskText = taskInput.value.trim();
    if (taskText === "") {
        alert("Please enter a task!");
        return;
    }
    var tasksList = document.getElementById("tasksList");
    var li = document.createElement("li");
    li.innerHTML = `
    <span>${taskText}</span>
    <button onclick="removeTask(this)">Remove</button>
  `;
    tasksList.appendChild(li);
    taskInput.value = "";
}
function removeTask(button, e) {
    e.preventDefault();
    var li = button.parentNode;
    var ul = li.parentNode;
    ul.removeChild(li);
}
function removeAllTasks(e) {
    e.preventDefault();
    var tasksList = document.getElementById("tasksList");
    tasksList.innerHTML = ""; // Clear the entire list
}
```
