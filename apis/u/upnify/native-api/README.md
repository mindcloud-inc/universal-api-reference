# Upnify: Native API Reference

A consolidated summary of Upnify's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://desarrollo.upnify.com/api-rest/
- **API base URL:** `https://api.upnify.com`

## Authentication

### Session Token Login

Authenticates with Upnify user credentials by calling /login and reuses the returned session token on later API requests.

### Credentials

- **Username:** `username` · required · Your Upnify user email or username used to sign in.
- **Password:** `password` · required · Your Upnify account password.

Send these headers with each API request:

```http
token: <custom.tkSesion>
```

[Official authentication documentation](https://desarrollo.upnify.com/api-rest/autenticacion/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `cantidadRegistros` in the query string to set the page size (default 50). Use `pagina` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST v4/clientes` | [docs](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-PostClientes) |
| [Create Company](actions/create-company.md) | `POST v4/empresas` | [docs](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-PostEmpresas) |
| [Create Product](actions/create-product.md) | `POST v4/catalogos/productos` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Productos-PostCatalogosProductos) |
| [Create Prospect](actions/create-prospect.md) | `POST v4/prospectos` | [docs](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-PostProspectos) |
| [Create Sale](actions/create-sale.md) | `POST v4/ventas` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-PostVentas) |
| [Create User](actions/create-user.md) | `POST v4/catalogos/usuarios` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-PostCatalogosUsuarios) |
| [Delete Client](actions/delete-client.md) | `DELETE v4/clientes/:tkCliente` | [docs](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-DeleteClientesTkcliente) |
| [Delete Company](actions/delete-company.md) | `DELETE v4/empresas/:tkEmpresa` | [docs](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-DeleteEmpresasTkempresa) |
| [Delete Opportunity](actions/delete-opportunity.md) | `DELETE v4/oportunidades/:tkOportunidad` | [docs](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-DeleteOportunidadesTkoportunidad) |
| [Delete Prospect](actions/delete-prospect.md) | `DELETE v4/prospectos/:tkProspecto` | [docs](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-DeleteProspectosTkprospecto) |
| [Delete Sale](actions/delete-sale.md) | `DELETE v4/ventas/:tkVenta` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-DeleteVentasTkventa) |
| [Delete User](actions/delete-user.md) | `DELETE v4/catalogos/usuarios/:tkUsuario` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-DeleteCatalogosUsuariosTkusuario) |
| [Get Client](actions/get-client.md) | `GET v4/clientes/:tkCliente` | [docs](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-GetClientesTkcliente) |
| [Get Company](actions/get-company.md) | `GET v4/empresas/:tkEmpresa` | [docs](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-GetEmpresasTkempresa) |
| [Get Opportunity](actions/get-opportunity.md) | `GET v4/oportunidades/:tkOportunidad` | [docs](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-GetOportunidadesTkoportunidad) |
| [Get Product](actions/get-product.md) | `GET v4/catalogos/productos/:tkProducto` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Productos-GetCatalogosProductosTkproducto) |
| [Get Prospect](actions/get-prospect.md) | `GET v4/prospectos/:tkProspecto` | [docs](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-GetProspectosTkprospecto) |
| [Get Sale](actions/get-sale.md) | `GET v4/ventas/:tkVenta` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentasTkventa) |
| [Get User](actions/get-user.md) | `GET v4/catalogos/usuarios/:tkUsuario` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-GetCatalogosUsuariosTkusuario) |
| [List Client Opportunities](actions/list-client-opportunities.md) | `GET v4/clientes/:tkCliente/oportunidades` | [docs](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-GetClientesTkclienteOportunidades) |
| [List Clients](actions/list-clients.md) | `GET v4/clientes` | [docs](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-GetClientes) |
| [List Companies](actions/list-companies.md) | `GET v4/empresas` | [docs](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-GetEmpresas) |
| [List Company Contacts](actions/list-company-contacts.md) | `GET v4/empresas/:tkEmpresa/contactos` | [docs](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-GetEmpresasTkempresaContactos) |
| [List Opportunities](actions/list-opportunities.md) | `GET v4/oportunidades` | [docs](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-GetOportunidades) |
| [List Opportunity Products](actions/list-opportunity-products.md) | `GET v4/oportunidades/:tkOportunidad/productos` | [docs](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-GetOportunidadesTkoportunidadProductos) |
| [List Products](actions/list-products.md) | `GET v4/catalogos/productos` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Productos-GetCatalogosProductos) |
| [List Prospect Opportunities](actions/list-prospect-opportunities.md) | `GET v4/prospectos/:tkProspecto/oportunidades` | [docs](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-GetProspectosTkprospectoOportunidades) |
| [List Prospects](actions/list-prospects.md) | `GET v4/prospectos` | [docs](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-GetProspectos) |
| [List Sale Payments](actions/list-sale-payments.md) | `GET v4/ventas/:tkVenta/cobros` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentasTkventaCobros) |
| [List Sale Products](actions/list-sale-products.md) | `GET v4/ventas/:tkVenta/productos` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentasTkventaProductos) |
| [List Sales](actions/list-sales.md) | `GET v4/ventas` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-GetVentas) |
| [List Sales Estimates](actions/list-sales-estimates.md) | `GET v4/oportunidades/estimacion` | [docs](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Estimacion_de_ventas-GetOportunidadesEstimacion) |
| [List Users](actions/list-users.md) | `GET v4/catalogos/usuarios` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-GetCatalogosUsuarios) |
| [Update Client](actions/update-client.md) | `PUT v4/clientes/:tkCliente` | [docs](https://desarrollo.upnify.com/api-rest/clientes/#api-Clientes-PutClientesTkcliente) |
| [Update Company](actions/update-company.md) | `PUT v4/empresas/:tkEmpresa` | [docs](https://desarrollo.upnify.com/api-rest/empresas/#api-Empresas-PutEmpresasTkempresa) |
| [Update Opportunity](actions/update-opportunity.md) | `PUT v4/oportunidades/:tkOportunidad` | [docs](https://desarrollo.upnify.com/api-rest/oportunidades/#api-Oportunidades-PutOportunidadesTkoportunidad) |
| [Update Product](actions/update-product.md) | `PUT v4/catalogos/productos/:tkProducto` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Productos-PutCatalogosProductosTkproducto) |
| [Update Prospect](actions/update-prospect.md) | `PUT v4/prospectos/:tkProspecto` | [docs](https://desarrollo.upnify.com/api-rest/prospectos/#api-Prospectos-PutProspectosTkprospecto) |
| [Update Sale](actions/update-sale.md) | `PUT v4/ventas/:tkVenta` | [docs](https://desarrollo.upnify.com/api-rest/ventas/#api-Ventas-PutVentasTkventa) |
| [Update User](actions/update-user.md) | `PUT v4/catalogos/usuarios/:tkUsuario` | [docs](https://desarrollo.upnify.com/api-rest/catalogos/#api-Usuarios-PutCatalogosUsuariosTkusuario) |
