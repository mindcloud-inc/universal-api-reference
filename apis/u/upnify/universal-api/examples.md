# Upnify Universal API Examples

These examples use the MindCloud API key and Upnify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Upnify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "activo": 1,
      "apellidos": "string",
      "avatar": "string",
      "cambiarPrecios": 1,
      "correoConfigurado": 1,
      "crearComunicaciones": 1,
      "crearDocumentos": 1,
      "crearEmpresas": 1,
      "crearEtiquetas": 1,
      "crearPlantillas": 1,
      "email": "ava@example.com",
      "estado": "string",
      "etiquetar": 1,
      "fuerzaContrasenia": "string",
      "gmt": 1,
      "grupo": "string",
      "hacerDescuentos": 1,
      "idioma": 1,
      "indice": 1,
      "iniciales": "string",
      "integrante": "string",
      "mantenimientoDb": 1,
      "movil": "string",
      "nivel": 1,
      "nombre": "string",
      "pais": "string",
      "puedeCancelarFactura": 1,
      "puedeCompartir": 1,
      "puedeExportar": 1,
      "puedeFacturar": 1,
      "puedeImportar": 1,
      "puedeReasignar": 1,
      "puesto": "string",
      "telefono": "string",
      "tituloNivel": "string",
      "tkGrupo": "string",
      "tkUsuario": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/upnify/latest/actions/list-users).

## Create Client

Creates a new client in Upnify.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nombre": "string",
  "empresa": "string",
  "telefono": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/upnify/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nombre": "string",
    "empresa": "string",
    "telefono": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "details": [
        {}
      ],
      "msg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/upnify/latest/actions/create-client).
