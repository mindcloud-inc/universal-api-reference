# Opportify: Analyze IP

Analyzes an IP address in Opportify for risk and geolocation.

```
GET https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-ip?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-ip?${params}`, {
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
| `ip` | string | yes | The IPv4 or IPv6 address to analyze. |
| `enableAI` | boolean | no | Enable AI-driven analysis for the IP address. Default is `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocklisted": {},
      "connectionType": "string",
      "geo": {},
      "hostReverse": "string",
      "ipAddress": "string",
      "ipAddressNumber": 1,
      "ipCidr": "string",
      "ipType": "string",
      "riskReport": {},
      "trustedProvider": {},
      "whois": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocklisted` | object | ### Block Listed Details  The `BlockListed` object provides detailed information about whether an IP address is listed in known blocklists and related data.   ---  #### Key Highlights: - **Continuous Monitoring**: We constantly monitor and update blocklist sources to ensure the information is accurate and reflects the latest active reports. - **Expanding Coverage**: Our system incorporates a wide range of trusted sources, with continuous efforts to onboard additional blocklist data providers.  ---  ### Response Elements |
| `connectionType` | string | The **connectionType** element provides information about the type of connection associated with a given IP address. Our system employs a **dynamic and evolving approach**, leveraging multiple data points to identify the connection type as accurately as possible.  - **wired**: A traditional wired connection (e.g., DSL, fiber, cable). - **mobile**: A mobile network connection (e.g., 4G, 5G). - **enterprise**: A connection from a known large business or corporate network. - **satellite**: A satellite internet connection. - **vpn**: A connection routed through a Virtual Private Network. - **cloud-provider**: A connection from a cloud hosting provider (e.g., AWS, Azure). - **open-proxy**: A connection using an open or public proxy. - **tor**: A connection routed through the Tor network. |
| `geo` | object | ### Geolocation Determination & Confidence Levels Geolocation details are derived by analyzing the provided IP address using data aggregated from a wide range of sources, both official and unofficial (such as user-generated data, open-source, or crowdsourced). This data is meticulously evaluated and ranked using a proprietary weighted reliability score that is tailored to the specific characteristics and trustworthiness of each data source.  ---  #### Confidence Levels  The geolocation process assigns a confidence level to each level of granularity. These levels reflect the probability of accuracy based on the reliability of the data and analysis:  - **Continent-Level (99%)**: The determination of the continent is highly reliable, with a near-certain accuracy rate of 99%. - **Country-Level (98%)**: Locating the specific country has a very high accuracy of 98%, reflecting reliable cross-verification. - **Region-Level (70–90%)**: Identifying regions (such as states or provinces) has moderate to high accuracy, depending on the data quality and density for the given area. - **City-Level (50–70%)**: Pinpointing the specific city is moderately accurate, influenced by factors such as ISP data resolution and urban vs. rural settings. - **Specific Area/Point (5–40%)**: Pinpointing a highly specific area (e.g., a neighborhood or street) has a significantly lower confidence level due to inherent limitations in IP-based geolocation technology.  ---  #### Key Features  - **Alphabetical Object Sorting**:     The keys in the returned geolocation object are consistently sorted alphabetically, ensuring a predictable structure for easier integration and parsing.  ---  ### Response Elements |
| `hostReverse` | string | Real time reverse DNS lookup result for the IP address. |
| `ipAddress` | string | The analyzed IP address. |
| `ipAddressNumber` | number | Numeric representation of the IP address. |
| `ipCidr` | string | CIDR notation of the IP address. |
| `ipType` | string | Type of the IP address (IPv4 or IPv6). |
| `riskReport` | object | ### Risk Level Determination This documentation outlines how the risk level is determined based on a `normalizedScore` generated by a **multivariate linear regression model**. The risk level provides a static representation of thresholds to classify the severity of risk for an entity.  #### How the Score is Generated  The risk score (`normalizedScore`) is computed using a **multivariate linear regression model**, a machine learning approach that evaluates multiple input features to predict the risk score.  ##### Key Features of the Model: 1. **Dynamic Scoring:** The model assigns weights to various risk factors, dynamically updating them based on training with new data. 2. **Constant Training:** The model is continuously retrained with the latest data to improve accuracy and adapt to evolving risk patterns. 3. **Scalability:** The model supports multiple features and their interactions, deriving a comprehensive and reliable risk score.  The output score is normalized to a range of **200–1000** for easier interpretation and alignment with industry practices.  ---  #### Risk Level Thresholds  The risk level is a static representation of the `normalizedScore`, categorized into five distinct levels:  \| **Risk Level** \| **Score Range**          \| **Description**                                                                 \| \|----------------\|--------------------------\|---------------------------------------------------------------------------------\| \| `highest`      \| `normalizedScore > 800` \| Represents the most critical level of risk. Immediate attention is required. **Extremely high likelihood of malicious IP activity or fraud.**   \| \| `high`         \| `600 < normalizedScore <= 800` \| Indicates a high level of risk. Consider mitigation actions promptly. **Strong likelihood of malicious IP activity or fraud.**          \| \| `medium`       \| `400 < normalizedScore <= 600` \| Reflects a moderate level of risk. Monitoring and possible action advised.     \| \| `low`          \| `300 < normalizedScore <= 400` \| Denotes a low level of risk. Regular monitoring is sufficient.                 \| \| `lowest`       \| `normalizedScore <= 300` \| The lowest level of risk. Risk is considered negligible or minimal.            \|  ---  #### Usage  This risk level determination serves as a human-readable representation of the machine learning model's output. It enables: - **Risk Monitoring:** Identifying entities that require immediate attention. - **Action Prioritization:** Guiding mitigation efforts based on the severity of the risk. - **Decision-Making:** Providing clear thresholds for automated and manual workflows.  ---  #### Key Notes 1. **Dynamic Scoring, Static Levels:**   - While the score is dynamically updated through a multivariate linear regression model, the risk levels remain static to maintain consistency and interpretability.  2. **Customizable Thresholds:**   - The thresholds for the levels are configurable based on organizational needs or domain-specific requirements.  3. **Model Retraining:**    - Regular updates to the model ensure that scores accurately reflect real-world risk trends, improving the reliability of level assignments.  ---  This approach combines the adaptability of multivariate linear regression with the simplicity of static thresholds, offering a robust framework for risk assessment and decision-making.  ---  ### Response Elements |
| `trustedProvider` | object | Details of trusted providers for an IP address. |
| `whois` | object | ### WHOIS Details This object provides sanitized and normalized WHOIS information for an IP address, including details about the Regional Internet Registry (RIR), Autonomous System Number (ASN), organization, and contact information.  #### Key Features: - **RIR Details**: Identify the Regional Internet Registry managing the IP address. - **ASN Information**: Obtain the Autonomous System Number details, including the ASN identifier, name, and description. - **Organization Data**: Retrieve organization details, such as the ID, name, type, description, address, country, and contact information. - **Contact Information**: Access contact details for abuse, admin, and tech issues, including the contact ID, type, name, address, phone, fax, and email.  ---  ### Response Elements |

## Native endpoint

Through the native Opportify API, this operation is `POST /ip/analyze` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-ip.md) for the provider-specific parameters and requirements.

