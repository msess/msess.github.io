---
name: MSESS Shirt
price: 20.99
produrl: https://msess.ca/products/tshirt.html
slug: MSESS-Shirt
sku: MSESSshirt2018-1
image: /img/shop/MSESSshirt2018.png
image_large: /img/shop/MSESSshirt2018_Large.png
custom1-name: "Size"
custom1-options: "Small|Medium|Large|XL"
custom1-value: "Medium"
layout: productdetails
---

<script>
  var stripe = Stripe('pk_live_wARa4mFGWVywv5pm543vz3c8', {
    betas: ['checkout_beta_3']
  });

  var checkoutButton = document.getElementById('checkout-button');
  checkoutButton.addEventListener('click', function () {
    // When the customer clicks on the button, redirect
    // them to Checkout.
    stripe.redirectToCheckout({
      items: [{sku: 'sku_E0PRxctI2GFjUR', quantity: 1}],
      successUrl: 'https://msess.ca/success',
      cancelUrl: 'https://msess.ca/canceled',
    })
    .then(function (result) {
      if (result.error) {
        // If `redirectToCheckout` fails due to a browser or network
        // error, display the localized error message to your customer.
        var displayError = document.getElementById('error-message');
        displayError.textContent = result.error.message;
      }
    });
  });
</script>


Rep your Major! The first MSESS shirt designed by our own Brindan Ramalingam. In a couple years this will be retro and vintage so pick this up now and have a lasting souvenir from your time as a MSE student.


The design on the shirt is printed graphics.

<img src="/img/shop/shirtSizing.jpg" alt="T-Shirt Sizing Chart" id="responsive-image" class="thumbnail"/>