# hello-world
change order of proceed to checkout and view shopping bag

<div class="popup-cart py-25 px-20 js-popup-cart-ajax" data-popup-content>
    <div class="popup-cart__head d-flex align-items-center">
        <h5 class="m-0">{{ 'general.popups.cart.title' | t }} <span data-js-popup-cart-count></span></h5>
        <i class="popup-cart__close ml-auto cursor-pointer" data-js-popup-close>{% render 'icon-theme-164' %}</i>
    </div>
    <div class="popup-cart__content d-none-important">
        <div class="popup-cart__items mt-15 border-bottom"></div>
        <div class="popup-cart__subtotal h5 d-flex align-items-center mt-15 mb-0">
            <p class="m-0">{{ 'general.popups.cart.subtotal' | t }}</p>
            <span class="ml-auto">
                <span class="price" data-js-popup-cart-subtotal></span>
            </span>
        </div>
        {%- if settings.cart_show_free_shipping -%}
            <div class="popup-cart__free-shipping my-20">
                {% render 'free-shipping' %}
            </div>
        {%- endif -%}
        <div class="popup-cart__buttons mt-15">
            <a href="{{ routes.root_url }}{% if routes.root_url != '/' %}/{% endif %}checkout" class="btn btn--full btn--secondary">{{ 'general.popups.cart.button_to_checkout' | t }}</a>
            <a href="{{ routes.cart_url }}" class="btn btn--full mt-20">{{ 'general.popups.cart.button_to_cart' | t }}</a>
        </div>
    </div>
    <div class="popup-cart__empty mt-20 d-none-important">{{ 'general.popups.cart.empty' | t }}</div>
</div>
