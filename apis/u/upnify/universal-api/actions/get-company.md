# Upnify: Get Company

Retrieves a company from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-company?connectionId=$CONNECTION_ID&tkEmpresa=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkEmpresa": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-company?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tkEmpresa` | string | yes | Código token que identifica de forma única a una empresa en el sistema, del cual se requiere obtener los detalles. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ciudad": "string",
      "codigoPostal": "string",
      "corporativo": "string",
      "cp1e": "string",
      "cp60e": "string",
      "direccion1": "string",
      "direccion2": "string",
      "eCatalogo1": "string",
      "eCatalogo2": "string",
      "eCatalogo3": "string",
      "ejecutivoNombre": "string",
      "empresa": "string",
      "estado": "string",
      "fechaCreacion": "string",
      "idEstado": "string",
      "idExterno": "string",
      "idMunicipio": "string",
      "idPais": "string",
      "indice": 1,
      "industria": "string",
      "municipio": "string",
      "numeroEmpleados": 1,
      "numeroExterior": "string",
      "numeroInterior": "string",
      "pais": "string",
      "telefonoCorporativo": "string",
      "tkCorporativo": "string",
      "tkEmpresa": "string",
      "tkIndustria": "string",
      "tkUsuario": "string",
      "ultimaModificacion": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ciudad` | string | Indica la ciudad donde se encuentra ubicada la empresa. |
| `codigoPostal` | string | Contiene el código de región postal de la empresa. |
| `corporativo` | string | Nombre del corporativo al que pertenece la empresa. |
| `cp1e` | string | Contiene el valor del primer campo personalizado para empresas, el cual es establecido por el usuario. |
| `cp60e` | string | Contiene el valor del sexagésimo campo personalizado para empresas, el cual es establecido por el usuario. |
| `direccion1` | string | Contiene la dirección de la empresa. |
| `direccion2` | string | Guarda una segunda dirección caso de que la empresa cuente con una dirección alternativa. |
| `eCatalogo1` | string | Primer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para empresas, los cuales son elegidos por el usuario. |
| `eCatalogo2` | string | Segundo catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para empresas, los cuales son elegidos por el usuario. |
| `eCatalogo3` | string | Tercer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para empresas, los cuales son elegidos por el usuario. |
| `ejecutivoNombre` | string | Guarda el nombre del ejecutivo que dío de alta en el sistema a la empresa. |
| `empresa` | string | Contiene el nombre de la empresa. |
| `estado` | string | Especifica el nombre del estado donde se encuentra la empresa. |
| `fechaCreacion` | string | Contiene un formato compuesto de fecha y hora que indica cuando fué dada de alta la empresa en el sistema. |
| `idEstado` | string | Especifica el id del estado donde se encuentra la empresa. |
| `idExterno` | string | Identificador unico, no obligatorio para la interconexión con sistemas externos. |
| `idMunicipio` | string | Contiene el id del municipio al que pertenece la empresa. |
| `idPais` | string | Guarda el id del país donde se ubica la empresa. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `industria` | string | Especifica a que tipo de insdustria pertenece la empresa. |
| `municipio` | string | Contiene el nombre del municipio al que pertenece la empresa. |
| `numeroEmpleados` | number | Especifica el número de empleados que tiene la empresa. |
| `numeroExterior` | string | Especifica un número exterior como parte de la dirreción de la empresa. |
| `numeroInterior` | string | Especifica un número interior como parte de la dirreción de la empresa. |
| `pais` | string | Guarda el nombre del país donde se ubica la empresa. |
| `telefonoCorporativo` | string | Guarda el número de telefono de la empresa (Si tiene un valor no númerico, devolvera un String). |
| `tkCorporativo` | string | Código token que identifica de forma única a una industria. |
| `tkEmpresa` | string | Código token que identifica de forma única a una empresa. |
| `tkIndustria` | string | Código token que identifica de forma única a que corporativo pertenece la empresa. |
| `tkUsuario` | string | Código token que identifica de forma única al ejecutivo de la empresa. |
| `ultimaModificacion` | string | Contiene un formato compuesto de fecha y hora que indica cuando fué la última modificación de la enmpresa. |
| `url` | string | Guarda la dirección del sitio web de la empresa. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/empresas/:tkEmpresa` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

