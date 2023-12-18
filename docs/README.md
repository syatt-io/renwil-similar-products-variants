# Renwil Similar Products Variants

The Similar Products Variants app returns similar products related to an SKU so users can select other dimensions of the same product.

![Screenshot 2023-12-18 at 17 09 23](https://github.com/syatt-io/renwil-similar-products-variants/assets/44602686/4ef83766-0856-42af-8df0-b174d4c94d11)

## Before you start
1. Set up similar products in your store’s **Products and SKU.** Access your store’s Admin and go to **Products > Catalog > Products and SKU**.
2. In **Products and SKU**, in the column **SKU**, click on the desired SKU.
3. In the field **Similar (Alternative Products)**, type the product name you desire

![similar-field](https://user-images.githubusercontent.com/67270558/147780337-ccc0d622-535e-47ce-9ede-d86f1d571546.gif)

4. Then, In **Products and SKU**, in the column **SKU**, click on the one you have added in the last step.

Now, follow the [app’s configuration below](#configuration) to show the similar products you have set up.


## Configuration

1. Using [VTEX IO CLI](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-vtex-io-cli-installation-and-command-reference), install the app by running the following:

```bash
vtex install renwil.similar-products-variants
```
2. Add the `renwil.similar-products-variants` app to your theme's dependencies in the `manifest.json`

```json
"dependencies": {
    "renwil.similar-products-variants": “0.x”
}
```

3. Add the `similar-products-variants` block to the product template you desire, such as `store.product`, to display a similar product list. 


```json
...
  "flex-layout.col#right-col": {
    "props": {
      "preventVerticalStretch": true,
      "rowGap": 0
    },
    "children": [
      "flex-layout.row#product-name",
      "product-rating-summary",
      "flex-layout.row#list-price-savings",
      "flex-layout.row#selling-price",
      "product-installments",
      "product-separator",
      "product-identifier.product",
      "sku-selector",
    + "similar-products-variants",
      "product-quantity",
      "link-seller",
      "product-availability",
      "product-assembly-options",
      "product-gifts",
      "flex-layout.row#buy-button",
      "availability-subscriber",
      "shipping-simulator",
      "share#default"
    ]
  },
...
```

## Customization

To apply CSS customizations in this and other blocks, follow the instructions given in the recipe on [Using CSS Handles for store customization](https://vtex.io/docs/recipes/style/using-css-handles-for-store-customization).

| CSS Handles            |
| -----------            |
| `variants`             |
| `title`                |
| `var-wrap`             |
| `link_wrap`             |
| `link_wrap--is-active`  |
| `text`                  |
