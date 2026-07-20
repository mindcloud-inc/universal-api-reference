# <img src="https://images.mindcloud.co/apps/icons/tiktok-shop-icon-logo-symbol-free-png_1770912979719.png" alt="TikTok Shop logo" width="28" height="28"> TikTok Shop: Universal API

TikTok Shop through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tikTokShop/latest
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://partner.tiktokshop.com/docv2/page/666012dd609d4402cc3be995?external_id=666012dd609d4402cc3be995

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authorized Shops](actions/get-authorized-shops.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-authorized-shops?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Authorized Shops

| Action | Method | Description |
| --- | --- | --- |
| [Get Authorized Shops](actions/get-authorized-shops.md) | GET |  |
| [Get Order Detail](actions/get-order-detail.md) | GET |  |
| [Get Package Shipping Document (v2)](actions/get-package-shipping-document-v2.md) | GET |  |

### Cash Flow Statement Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Statements](actions/get-statements.md) | GET |  |
| [Get Transactions by Statement](actions/get-transactions-by-statement.md) | GET |  |

### Getpackagedetail

| Action | Method | Description |
| --- | --- | --- |
| [Get Package Detail](actions/get-package-detail.md) | GET | Returns information about a package, including handover time slot, tracking number, and shipping provider information. |

### Getshippingproviders

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipping Providers](actions/get-shipping-providers.md) | GET | This API is used to obtain the shipping provider corresponding to the specified delivery option. |

### Gwdo

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouse Delivery Options](actions/get-warehouse-delivery-options.md) | GET | This API is used to obtain a list of delivery options available through the seller's designated warehouse. |

### Gwh

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouse List](actions/get-warehouse-list.md) | GET | This API retrieves all warehouse information associated with the seller. Warehouse information includes name, status, address, and other… |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Inventory](actions/get-product-inventory.md) | GET | Use this api to get product stock details. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Update Inventory](actions/update-inventory.md) | PUT |  |

### Order Fulfillment

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Order](actions/cancel-order.md) | PUT | Use this API to cancel an order on behalf of a seller. In the US and UK markets, when an item is out of stock, partial cancellation on the… |
| [Split Orders](actions/split-orders.md) | POST | Use this API to confirm an order split. Note that ​​supported split levels vary by region​​: - Some regions support ​​item-level splits​​… |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Mark Package As Shipped](actions/mark-package-as-shipped.md) | POST | This API is currently exclusive to the following markets: US, UK, ES, IE. This API is for sellers who fulfill orders through their own… |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Packages](actions/create-packages.md) | POST |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Get Product](actions/get-product.md) | GET | Retrieve all properties of a product that is in the DRAFT, PENDING, or ACTIVATE status. |
| [Search Products](actions/search-products.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Order List](actions/get-order-list.md) | GET |  |

### Shippackage

| Action | Method | Description |
| --- | --- | --- |
| [Ship Package](actions/ship-package.md) | PUT | Use this API to ship a package. There are two kinds of shipping options available: TikTok Shipping or Seller Shipping. - TikTok Shipping:… |

### Shipping Service

| Action | Method | Description |
| --- | --- | --- |
| [List Eligible Shipping Service](actions/list-eligible-shipping-service.md) | GET | Use this API ( for US ) to query the list of available shipping services when specifying packages' size or weight. The shipping fee and… |

### Tiktok Shipping

| Action | Method | Description |
| --- | --- | --- |
| [Get Package Shipping Document](actions/get-package-shipping-document.md) | GET | For orders shipped by TikTok Shop, this API retrieves the URL of shipping documents (shipping label and packing slip) for a package… |

