<!doctype html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="ClothesTeen: Moda juvenil a tu alcance. Encuentra lo último en tendencias para hombres y mujeres.">
    <meta name="keywords" content="moda juvenil, ropa, hombres, mujeres, tienda de ropa">
    <title>ClothesTeen</title>
    <link rel="stylesheet" href="ClothesTeen.css">
</head>
<body id="mainBody" style="overflow: auto;">
    <header>
        <center><h1>ClothesTeen</h1></center>
        <center>
            <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Logo+A.png" alt="Logotipo de ClothesTeen" width="200" title="Nuestro Logo">
        </center>
        <nav>
            <ul>
                <li><a href="Men.html">Hombre</a></li>
                <li><a href="Women.html">Mujer</a></li>
            </ul>
        </nav>
    </header>

    <hr>

    <div class="filter-container">
        <button class="filter-button" onclick="filterCategory('all')">Todos</button>
        <button class="filter-button" onclick="filterCategory('ropa')">Ropa</button>
        <button class="filter-button" onclick="filterCategory('zapatos')">Zapatos</button>
        <button class="filter-button" onclick="filterCategory('accesorios')">Accesorios</button>
    </div>

    <center>
        <div class="search-container">
            <label for="searchBar" hidden>Buscar productos:</label>
            <input type="text" id="searchBar" class="search-bar" placeholder="Buscar productos..." oninput="showSuggestions()">
            <div id="suggestions" class="suggestions-box"></div>
            <button class="search-button" onclick="searchProducts()">Buscar</button>
        </div>
    </center>

    <div class="cart-container">
        <button class="cart-button" onclick="toggleCart()">
            <i class="fas fa-shopping-cart"></i> 🛒Carrito (<span id="cartCount">0</span>)
        </button>
        <div id="cartDropdown" class="cart-dropdown">
            <p id="cartContent">Tu carrito está vacío.</p>
            <button class="filter-button" onclick="clearCart()">Vaciar carrito</button>
            <button class="filter-button" onclick="goToCart()">Ir a comprar</button>
        </div>
    </div>

    <hr>

    <section class="products-container">
        <h3>Productos disponibles</h3>
        <div id="products" class="product-list">
            <!-- Producto 1 -->
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Camisa Azul.png" alt="Camisa Azul" width="200">
                <p>Camisa Azul - Q25</p>
                <p>Tallas: S, M, L</p>
                <p>Colores: Azul, Blanco</p>
                <button class="filter-button" onclick="addToCart('Camisa Azul', 25)">Agregar al carrito</button>
            </div>
            
            <!-- Producto 2 -->
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Camisa Verde.png" alt="Camisa Verde" width="110">
                <p>Camisa Verde - Q30</p>
                <p>Tallas: M, L</p>
                <p>Colores: Verde, Negro</p>
                <button class="filter-button" onclick="addToCart('Camisa Verde', 30)">Agregar al carrito</button>
            </div>
            
            <!-- Producto 3 -->
            <div class="product zapatos">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Zapatos deportivos.png" alt="Zapatos Deportivos" width="165">
                <p>Zapatos Deportivos - Q45</p>
                <p>Tallas: 39, 40, 42</p>
                <p>Colores: Blanco, Gris</p>
                <button class="filter-button" onclick="addToCart('Zapatos Deportivos', 45)">Agregar al carrito</button>
            </div>

            <!-- Producto 4 -->
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Chaqueta Cuero.png" alt="Chaqueta de Cuero" width="200">
                <p>Chaqueta de Cuero - Q120</p>
                <p>Tallas: M, L, XL</p>
                <p>Colores: Negro, Marrón</p>
                <button class="filter-button" onclick="addToCart('Chaqueta de Cuero', 120)">Agregar al carrito</button>
            </div>

            <!-- Producto 5 -->
            <div class="product accesorios">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Gorra negra.jpeg" alt="Gorra Negra">
                <p>Gorra Negra - Q5</p>
                <p>Colores: Negro, Blanco</p>
                <button class="filter-button" onclick="addToCart('Gorra Negra', 15)">Agregar al carrito</button>
            </div>

            <!-- Producto 6 -->
            <div class="product accesorios">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Mochila.jpeg" alt="Mochila">
                <p>Mochila - Q35</p>
                <p>Colores: Negro, Azul</p>
                <button class="filter-button" onclick="addToCart('Mochila', 35)">Agregar al carrito</button>
            </div>
            
            <!-- Producto 7 -->
            <div class="product zapatos">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Botas cuero.jpeg" alt="Botas de Cuero">
                <p>Botas de Cuero - Q90</p>
                <p>Tallas: 40, 41, 43</p>
                <p>Colores: Marrón, Negro</p>
                <button class="filter-button" onclick="addToCart('Botas de Cuero', 90)">Agregar al carrito</button>
            </div>

            <!-- Producto 8 -->
            <div class="product ropa">
                <img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Falda negra.jpeg" alt="Falda Negra">
                <p>Falda Negra - Q20</p>
                <p>Tallas: S, M</p>
                <p>Colores: Negro, Rojo</p>
                <button class="filter-button" onclick="addToCart('Falda Negra', 20)">Agregar al carrito</button>
            </div>
        </div>
    </section>

    <div id="notification"></div>

    <footer>
        <div class="contact-info">
            <p>Teléfono de contacto: 5973-5460</p>
        </div>
        <div class="social-media">
            <a  href="ClothesTeen.html"><img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Instagram.jpeg" width="50"></a> 
			<a href="#"><img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\Facebook.png" width="50"></a> 
			<a href="#"><img src="C:\Users\javir\OneDrive\Escritorio\Proyecto Progra\Imagenes\X.png" width="50"></a>
        </div>
		
		<p>&copy; 2024 ClothesTeen. Todos los derechos reservados.</p>
    </footer>

    <script>
        let cart = JSON.parse(localStorage.getItem('cart')) || [];
        let reviews = JSON.parse(localStorage.getItem('reviews')) || [];

        function toggleCart() {
            let cartDropdown = document.getElementById('cartDropdown');
            cartDropdown.style.display = (cartDropdown.style.display === 'block') ? 'none' : 'block';
        }

        function clearCart() {
            cart = [];
            updateCart();
        }

        function goToCart() {
            window.location.href = "carrito.html";
        }

        function updateCart() {
            localStorage.setItem('cart', JSON.stringify(cart));
            let cartCount = document.getElementById('cartCount');
            let cartContent = document.getElementById('cartContent');
            cartCount.innerText = cart.length;
            cartContent.innerHTML = cart.length === 0 ? "Tu carrito está vacío." : cart.map(item => `${item.name} - $${item.price}`).join('<br>');
        }

        function addToCart(productName, productPrice) {
            cart.push({ name: productName, price: productPrice });
            updateCart();
        }

        function filterCategory(category) {
            let products = document.getElementsByClassName('product');
            for (let i = 0; i < products.length; i++) {
                if (category === 'all' || products[i].classList.contains(category)) {
                    products[i].style.display = 'block';
                } else {
                    products[i].style.display = 'none';
                }
            }
        }

        function showSuggestions() {
            let input = document.getElementById('searchBar').value.toLowerCase();
            let suggestions = document.getElementById('suggestions');
            let products = document.getElementsByClassName('product');
            suggestions.innerHTML = '';
            for (let i = 0; i < products.length; i++) {
                let productName = products[i].querySelector('p').innerText.toLowerCase();
                if (productName.includes(input)) {
                    let suggestion = document.createElement('div');
                    suggestion.className = 'suggestion';
                    suggestion.innerText = productName;
                    suggestion.onclick = function () {
                        searchBar.value = productName;
                        searchProducts();
                    };
                    suggestions.appendChild(suggestion);
                }
            }
        }

        function searchProducts() {
            let input = document.getElementById('searchBar').value.toLowerCase();
            let products = document.getElementsByClassName('product');
            for (let i = 0; i < products.length; i++) {
                let productName = products[i].querySelector('p').innerText.toLowerCase();
                products[i].style.display = productName.includes(input) ? 'block' : 'none';
            }
        }

        updateCart();
    </script>
</body>
</html>
