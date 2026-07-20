# Bedrijfsdata.nl: List Currency Rates



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/list-currency-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/list-currency-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/list-currency-rates?${params}`, {
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
| `currency` | string | no | Base currency code, for example EUR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "currency": {
        "aave": 1,
        "ada": 1,
        "aed": 1,
        "afn": 1,
        "agix": 1,
        "akt": 1,
        "algo": 1,
        "all": 1,
        "amd": 1,
        "amp": 1,
        "ang": 1,
        "aoa": 1,
        "ape": 1,
        "apt": 1,
        "ar": 1,
        "arb": 1,
        "ars": 1,
        "atom": 1,
        "ats": 1,
        "aud": 1,
        "avax": 1,
        "awg": 1,
        "axs": 1,
        "azm": 1,
        "azn": 1,
        "bake": 1,
        "bam": 1,
        "bat": 1,
        "bbd": 1,
        "bch": 1,
        "bdt": 1,
        "bef": 1,
        "bgn": 1,
        "bhd": 1,
        "bif": 1,
        "bmd": 1,
        "bnb": 1,
        "bnd": 1,
        "bob": 1,
        "brl": 1,
        "bsd": 1,
        "bsv": 1,
        "bsw": 1,
        "btc": 1,
        "btg": 1,
        "btn": 1,
        "btt": 1,
        "busd": 1,
        "bwp": 1,
        "byn": 1,
        "byr": 1,
        "bzd": 1,
        "cad": 1,
        "cake": 1,
        "cdf": 1,
        "celo": 1,
        "cfx": 1,
        "chf": 1,
        "chz": 1,
        "clp": 1,
        "cnh": 1,
        "cny": 1,
        "comp": 1,
        "cop": 1,
        "crc": 1,
        "cro": 1,
        "crv": 1,
        "cspr": 1,
        "cuc": 1,
        "cup": 1,
        "cve": 1,
        "cvx": 1,
        "cyp": 1,
        "czk": 1,
        "dai": 1,
        "dash": 1,
        "dcr": 1,
        "dem": 1,
        "dfi": 1,
        "djf": 1,
        "dkk": 1,
        "doge": 1,
        "dop": 1,
        "dot": 1,
        "dydx": 1,
        "dzd": 1,
        "eek": 1,
        "egld": 1,
        "egp": 1,
        "enj": 1,
        "eos": 1,
        "ern": 1,
        "esp": 1,
        "etb": 1,
        "etc": 1,
        "eth": 1,
        "eur": 1,
        "eurc": 1,
        "fei": 1,
        "fil": 1,
        "fim": 1,
        "fjd": 1,
        "fkp": 1,
        "flow": 1,
        "flr": 1,
        "frax": 1,
        "frf": 1,
        "ftt": 1,
        "gala": 1,
        "gbp": 1,
        "gel": 1,
        "ggp": 1,
        "ghc": 1,
        "ghs": 1,
        "gip": 1,
        "gmd": 1,
        "gmx": 1,
        "gnf": 1,
        "gno": 1,
        "grd": 1,
        "grt": 1,
        "gt": 1,
        "gtq": 1,
        "gusd": 1,
        "gyd": 1,
        "hbar": 1,
        "hkd": 1,
        "hnl": 1,
        "hnt": 1,
        "hot": 1,
        "hrk": 1,
        "ht": 1,
        "htg": 1,
        "huf": 1,
        "icp": 1,
        "idr": 1,
        "iep": 1,
        "ils": 1,
        "imp": 1,
        "imx": 1,
        "inj": 1,
        "inr": 1,
        "iqd": 1,
        "irr": 1,
        "isk": 1,
        "itl": 1,
        "jep": 1,
        "jmd": 1,
        "jod": 1,
        "jpy": 1,
        "kas": 1,
        "kava": 1,
        "kcs": 1,
        "kda": 1,
        "kes": 1,
        "kgs": 1,
        "khr": 1,
        "kmf": 1,
        "knc": 1,
        "kpw": 1,
        "krw": 1,
        "ksm": 1,
        "kwd": 1,
        "kyd": 1,
        "kzt": 1,
        "lak": 1,
        "lbp": 1,
        "ldo": 1,
        "leo": 1,
        "link": 1,
        "lkr": 1,
        "lrc": 1,
        "lrd": 1,
        "lsl": 1,
        "ltc": 1,
        "ltl": 1,
        "luf": 1,
        "luna": 1,
        "lunc": 1,
        "lvl": 1,
        "lyd": 1,
        "mad": 1,
        "mana": 1,
        "mbx": 1,
        "mdl": 1,
        "mga": 1,
        "mgf": 1,
        "mina": 1,
        "mkd": 1,
        "mkr": 1,
        "mmk": 1,
        "mnt": 1,
        "mop": 1,
        "mro": 1,
        "mru": 1,
        "mtl": 1,
        "mur": 1,
        "mvr": 1,
        "mwk": 1,
        "mxn": 1,
        "mxv": 1,
        "myr": 1,
        "mzm": 1,
        "mzn": 1,
        "nad": 1,
        "near": 1,
        "neo": 1,
        "nexo": 1,
        "nft": 1,
        "ngn": 1,
        "nio": 1,
        "nlg": 1,
        "nok": 1,
        "npr": 1,
        "nzd": 1,
        "okb": 1,
        "omr": 1,
        "one": 1,
        "op": 1,
        "ordi": 1,
        "pab": 1,
        "paxg": 1,
        "pen": 1,
        "pepe": 1,
        "pgk": 1,
        "php": 1,
        "pi": 1,
        "pkr": 1,
        "pln": 1,
        "pol": 1,
        "pte": 1,
        "pyg": 1,
        "qar": 1,
        "qnt": 1,
        "qtum": 1,
        "rol": 1,
        "ron": 1,
        "rpl": 1,
        "rsd": 1,
        "rub": 1,
        "rune": 1,
        "rvn": 1,
        "rwf": 1,
        "sand": 1,
        "sar": 1,
        "sbd": 1,
        "scr": 1,
        "sdd": 1,
        "sdg": 1,
        "sek": 1,
        "sgd": 1,
        "shib": 1,
        "shp": 1,
        "sit": 1,
        "skk": 1,
        "sle": 1,
        "sll": 1,
        "snx": 1,
        "sol": 1,
        "sos": 1,
        "spl": 1,
        "srd": 1,
        "srg": 1,
        "ssp": 1,
        "std": 1,
        "stn": 1,
        "stx": 1,
        "sui": 1,
        "svc": 1,
        "syp": 1,
        "szl": 1,
        "thb": 1,
        "theta": 1,
        "tjs": 1,
        "tmm": 1,
        "tmt": 1,
        "tnd": 1,
        "ton": 1,
        "top": 1,
        "trl": 1,
        "trx": 1,
        "try": 1,
        "ttd": 1,
        "tusd": 1,
        "tvd": 1,
        "twd": 1,
        "twt": 1,
        "tzs": 1,
        "uah": 1,
        "ugx": 1,
        "uni": 1,
        "usd": 1,
        "usdc": 1,
        "usdd": 1,
        "usdp": 1,
        "usdt": 1,
        "uyu": 1,
        "uzs": 1,
        "val": 1,
        "veb": 1,
        "ved": 1,
        "vef": 1,
        "ves": 1,
        "vet": 1,
        "vnd": 1,
        "vuv": 1,
        "waves": 1,
        "wemix": 1,
        "woo": 1,
        "wst": 1,
        "xaf": 1,
        "xag": 1,
        "xau": 1,
        "xaut": 1,
        "xbt": 1,
        "xcd": 1,
        "xcg": 1,
        "xch": 1,
        "xdc": 1,
        "xdr": 1,
        "xec": 1,
        "xem": 1,
        "xlm": 1,
        "xmr": 1,
        "xof": 1,
        "xpd": 1,
        "xpf": 1,
        "xpt": 1,
        "xrp": 1,
        "xtz": 1,
        "yer": 1,
        "zar": 1,
        "zec": 1,
        "zil": 1,
        "zmk": 1,
        "zmw": 1,
        "zwd": 1,
        "zwg": 1,
        "zwl": 1
      },
      "date": "2026-05-07T12:00:00.000Z",
      "found": 1,
      "fromCurrency": "string",
      "monthlyCredits": 1,
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `currency.aave` | number |  |
| `currency.ada` | number |  |
| `currency.aed` | number |  |
| `currency.afn` | number |  |
| `currency.agix` | number |  |
| `currency.akt` | number |  |
| `currency.algo` | number |  |
| `currency.all` | number |  |
| `currency.amd` | number |  |
| `currency.amp` | number |  |
| `currency.ang` | number |  |
| `currency.aoa` | number |  |
| `currency.ape` | number |  |
| `currency.apt` | number |  |
| `currency.ar` | number |  |
| `currency.arb` | number |  |
| `currency.ars` | number |  |
| `currency.atom` | number |  |
| `currency.ats` | number |  |
| `currency.aud` | number |  |
| `currency.avax` | number |  |
| `currency.awg` | number |  |
| `currency.axs` | number |  |
| `currency.azm` | number |  |
| `currency.azn` | number |  |
| `currency.bake` | number |  |
| `currency.bam` | number |  |
| `currency.bat` | number |  |
| `currency.bbd` | number |  |
| `currency.bch` | number |  |
| `currency.bdt` | number |  |
| `currency.bef` | number |  |
| `currency.bgn` | number |  |
| `currency.bhd` | number |  |
| `currency.bif` | number |  |
| `currency.bmd` | number |  |
| `currency.bnb` | number |  |
| `currency.bnd` | number |  |
| `currency.bob` | number |  |
| `currency.brl` | number |  |
| `currency.bsd` | number |  |
| `currency.bsv` | number |  |
| `currency.bsw` | number |  |
| `currency.btc` | number |  |
| `currency.btg` | number |  |
| `currency.btn` | number |  |
| `currency.btt` | number |  |
| `currency.busd` | number |  |
| `currency.bwp` | number |  |
| `currency.byn` | number |  |
| `currency.byr` | number |  |
| `currency.bzd` | number |  |
| `currency.cad` | number |  |
| `currency.cake` | number |  |
| `currency.cdf` | number |  |
| `currency.celo` | number |  |
| `currency.cfx` | number |  |
| `currency.chf` | number |  |
| `currency.chz` | number |  |
| `currency.clp` | number |  |
| `currency.cnh` | number |  |
| `currency.cny` | number |  |
| `currency.comp` | number |  |
| `currency.cop` | number |  |
| `currency.crc` | number |  |
| `currency.cro` | number |  |
| `currency.crv` | number |  |
| `currency.cspr` | number |  |
| `currency.cuc` | number |  |
| `currency.cup` | number |  |
| `currency.cve` | number |  |
| `currency.cvx` | number |  |
| `currency.cyp` | number |  |
| `currency.czk` | number |  |
| `currency.dai` | number |  |
| `currency.dash` | number |  |
| `currency.dcr` | number |  |
| `currency.dem` | number |  |
| `currency.dfi` | number |  |
| `currency.djf` | number |  |
| `currency.dkk` | number |  |
| `currency.doge` | number |  |
| `currency.dop` | number |  |
| `currency.dot` | number |  |
| `currency.dydx` | number |  |
| `currency.dzd` | number |  |
| `currency.eek` | number |  |
| `currency.egld` | number |  |
| `currency.egp` | number |  |
| `currency.enj` | number |  |
| `currency.eos` | number |  |
| `currency.ern` | number |  |
| `currency.esp` | number |  |
| `currency.etb` | number |  |
| `currency.etc` | number |  |
| `currency.eth` | number |  |
| `currency.eur` | number |  |
| `currency.eurc` | number |  |
| `currency.fei` | number |  |
| `currency.fil` | number |  |
| `currency.fim` | number |  |
| `currency.fjd` | number |  |
| `currency.fkp` | number |  |
| `currency.flow` | number |  |
| `currency.flr` | number |  |
| `currency.frax` | number |  |
| `currency.frf` | number |  |
| `currency.ftt` | number |  |
| `currency.gala` | number |  |
| `currency.gbp` | number |  |
| `currency.gel` | number |  |
| `currency.ggp` | number |  |
| `currency.ghc` | number |  |
| `currency.ghs` | number |  |
| `currency.gip` | number |  |
| `currency.gmd` | number |  |
| `currency.gmx` | number |  |
| `currency.gnf` | number |  |
| `currency.gno` | number |  |
| `currency.grd` | number |  |
| `currency.grt` | number |  |
| `currency.gt` | number |  |
| `currency.gtq` | number |  |
| `currency.gusd` | number |  |
| `currency.gyd` | number |  |
| `currency.hbar` | number |  |
| `currency.hkd` | number |  |
| `currency.hnl` | number |  |
| `currency.hnt` | number |  |
| `currency.hot` | number |  |
| `currency.hrk` | number |  |
| `currency.ht` | number |  |
| `currency.htg` | number |  |
| `currency.huf` | number |  |
| `currency.icp` | number |  |
| `currency.idr` | number |  |
| `currency.iep` | number |  |
| `currency.ils` | number |  |
| `currency.imp` | number |  |
| `currency.imx` | number |  |
| `currency.inj` | number |  |
| `currency.inr` | number |  |
| `currency.iqd` | number |  |
| `currency.irr` | number |  |
| `currency.isk` | number |  |
| `currency.itl` | number |  |
| `currency.jep` | number |  |
| `currency.jmd` | number |  |
| `currency.jod` | number |  |
| `currency.jpy` | number |  |
| `currency.kas` | number |  |
| `currency.kava` | number |  |
| `currency.kcs` | number |  |
| `currency.kda` | number |  |
| `currency.kes` | number |  |
| `currency.kgs` | number |  |
| `currency.khr` | number |  |
| `currency.kmf` | number |  |
| `currency.knc` | number |  |
| `currency.kpw` | number |  |
| `currency.krw` | number |  |
| `currency.ksm` | number |  |
| `currency.kwd` | number |  |
| `currency.kyd` | number |  |
| `currency.kzt` | number |  |
| `currency.lak` | number |  |
| `currency.lbp` | number |  |
| `currency.ldo` | number |  |
| `currency.leo` | number |  |
| `currency.link` | number |  |
| `currency.lkr` | number |  |
| `currency.lrc` | number |  |
| `currency.lrd` | number |  |
| `currency.lsl` | number |  |
| `currency.ltc` | number |  |
| `currency.ltl` | number |  |
| `currency.luf` | number |  |
| `currency.luna` | number |  |
| `currency.lunc` | number |  |
| `currency.lvl` | number |  |
| `currency.lyd` | number |  |
| `currency.mad` | number |  |
| `currency.mana` | number |  |
| `currency.mbx` | number |  |
| `currency.mdl` | number |  |
| `currency.mga` | number |  |
| `currency.mgf` | number |  |
| `currency.mina` | number |  |
| `currency.mkd` | number |  |
| `currency.mkr` | number |  |
| `currency.mmk` | number |  |
| `currency.mnt` | number |  |
| `currency.mop` | number |  |
| `currency.mro` | number |  |
| `currency.mru` | number |  |
| `currency.mtl` | number |  |
| `currency.mur` | number |  |
| `currency.mvr` | number |  |
| `currency.mwk` | number |  |
| `currency.mxn` | number |  |
| `currency.mxv` | number |  |
| `currency.myr` | number |  |
| `currency.mzm` | number |  |
| `currency.mzn` | number |  |
| `currency.nad` | number |  |
| `currency.near` | number |  |
| `currency.neo` | number |  |
| `currency.nexo` | number |  |
| `currency.nft` | number |  |
| `currency.ngn` | number |  |
| `currency.nio` | number |  |
| `currency.nlg` | number |  |
| `currency.nok` | number |  |
| `currency.npr` | number |  |
| `currency.nzd` | number |  |
| `currency.okb` | number |  |
| `currency.omr` | number |  |
| `currency.one` | number |  |
| `currency.op` | number |  |
| `currency.ordi` | number |  |
| `currency.pab` | number |  |
| `currency.paxg` | number |  |
| `currency.pen` | number |  |
| `currency.pepe` | number |  |
| `currency.pgk` | number |  |
| `currency.php` | number |  |
| `currency.pi` | number |  |
| `currency.pkr` | number |  |
| `currency.pln` | number |  |
| `currency.pol` | number |  |
| `currency.pte` | number |  |
| `currency.pyg` | number |  |
| `currency.qar` | number |  |
| `currency.qnt` | number |  |
| `currency.qtum` | number |  |
| `currency.rol` | number |  |
| `currency.ron` | number |  |
| `currency.rpl` | number |  |
| `currency.rsd` | number |  |
| `currency.rub` | number |  |
| `currency.rune` | number |  |
| `currency.rvn` | number |  |
| `currency.rwf` | number |  |
| `currency.sand` | number |  |
| `currency.sar` | number |  |
| `currency.sbd` | number |  |
| `currency.scr` | number |  |
| `currency.sdd` | number |  |
| `currency.sdg` | number |  |
| `currency.sek` | number |  |
| `currency.sgd` | number |  |
| `currency.shib` | number |  |
| `currency.shp` | number |  |
| `currency.sit` | number |  |
| `currency.skk` | number |  |
| `currency.sle` | number |  |
| `currency.sll` | number |  |
| `currency.snx` | number |  |
| `currency.sol` | number |  |
| `currency.sos` | number |  |
| `currency.spl` | number |  |
| `currency.srd` | number |  |
| `currency.srg` | number |  |
| `currency.ssp` | number |  |
| `currency.std` | number |  |
| `currency.stn` | number |  |
| `currency.stx` | number |  |
| `currency.sui` | number |  |
| `currency.svc` | number |  |
| `currency.syp` | number |  |
| `currency.szl` | number |  |
| `currency.thb` | number |  |
| `currency.theta` | number |  |
| `currency.tjs` | number |  |
| `currency.tmm` | number |  |
| `currency.tmt` | number |  |
| `currency.tnd` | number |  |
| `currency.ton` | number |  |
| `currency.top` | number |  |
| `currency.trl` | number |  |
| `currency.trx` | number |  |
| `currency.try` | number |  |
| `currency.ttd` | number |  |
| `currency.tusd` | number |  |
| `currency.tvd` | number |  |
| `currency.twd` | number |  |
| `currency.twt` | number |  |
| `currency.tzs` | number |  |
| `currency.uah` | number |  |
| `currency.ugx` | number |  |
| `currency.uni` | number |  |
| `currency.usd` | number |  |
| `currency.usdc` | number |  |
| `currency.usdd` | number |  |
| `currency.usdp` | number |  |
| `currency.usdt` | number |  |
| `currency.uyu` | number |  |
| `currency.uzs` | number |  |
| `currency.val` | number |  |
| `currency.veb` | number |  |
| `currency.ved` | number |  |
| `currency.vef` | number |  |
| `currency.ves` | number |  |
| `currency.vet` | number |  |
| `currency.vnd` | number |  |
| `currency.vuv` | number |  |
| `currency.waves` | number |  |
| `currency.wemix` | number |  |
| `currency.woo` | number |  |
| `currency.wst` | number |  |
| `currency.xaf` | number |  |
| `currency.xag` | number |  |
| `currency.xau` | number |  |
| `currency.xaut` | number |  |
| `currency.xbt` | number |  |
| `currency.xcd` | number |  |
| `currency.xcg` | number |  |
| `currency.xch` | number |  |
| `currency.xdc` | number |  |
| `currency.xdr` | number |  |
| `currency.xec` | number |  |
| `currency.xem` | number |  |
| `currency.xlm` | number |  |
| `currency.xmr` | number |  |
| `currency.xof` | number |  |
| `currency.xpd` | number |  |
| `currency.xpf` | number |  |
| `currency.xpt` | number |  |
| `currency.xrp` | number |  |
| `currency.xtz` | number |  |
| `currency.yer` | number |  |
| `currency.zar` | number |  |
| `currency.zec` | number |  |
| `currency.zil` | number |  |
| `currency.zmk` | number |  |
| `currency.zmw` | number |  |
| `currency.zwd` | number |  |
| `currency.zwg` | number |  |
| `currency.zwl` | number |  |
| `date` | date |  |
| `found` | number |  |
| `fromCurrency` | string |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /currency` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currency-rates.md) for the provider-specific parameters and requirements.

