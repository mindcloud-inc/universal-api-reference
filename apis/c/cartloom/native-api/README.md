# Cartloom: Native API Reference

A consolidated summary of Cartloom's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://support.cartloom.com/hc/en-us/sections/115000264307-API
- **API base URL:** `https://mindcloudstage0424.cartloom.com/api`

## Authentication

### API Key

Use the Cartloom REST API key as the X-API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://support.cartloom.com/hc/en-us/articles/115000936168-API-Overview)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Discount](actions/add-discount.md) | `POST /discounts/add/format/json` | [docs](https://support.cartloom.com/hc/en-us/articles/115000892927-Add-Discount) |
| [Get Discount](actions/get-discount.md) | `POST /discounts/get/format/json` | [docs](https://support.cartloom.com/hc/en-us/articles/115000936228-Get-Discount) |
| [Get Order](actions/get-order.md) | `POST /orders/get/format/json` | [docs](https://support.cartloom.com/hc/en-us/articles/115000936188-Get-Order) |
| [List Discounts](actions/list-discounts.md) | `POST /discounts/list/format/json` | [docs](https://support.cartloom.com/hc/en-us/articles/115000936208-List-Discounts) |
| [List Orders](actions/list-orders.md) | `POST /orders/list/format/json` | [docs](https://support.cartloom.com/hc/en-us/articles/115000892907-List-Orders) |
