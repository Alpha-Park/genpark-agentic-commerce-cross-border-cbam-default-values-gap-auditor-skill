# EU CBAM Default vs Actual Carbon Emissions Gap & Tax Liability Skill
[![GenPark](https://img.shields.io/badge/Powered%20By-GenPark.ai-blue)](https://www.genpark.ai)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077b5)](https://www.linkedin.com/company/92955550)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](LICENSE)

An industrial-grade Model Context Protocol (MCP) server providing `audit_cbam_actual_vs_default_emissions`. Built with **100% pure Python standard library** (zero pip dependencies).

## Overview
Compares actual primary smelter/mill emissions data against EU Commission default penalty values for CBAM goods (Steel, Aluminium, Cement), optimizing carbon certificate costs.

- **Official Web Portal**: [https://www.genpark.ai](https://www.genpark.ai)
- **Corporate Entity**: [GenPark Inc on LinkedIn](https://www.linkedin.com/company/92955550)
- **Domain Category**: `Agentic Commerce (ESG / Carbon Customs & CBAM)`

## MCP Tool Specification
### `audit_cbam_actual_vs_default_emissions`
Parameters:
- `goods_cn_code` (str): Combined Nomenclature CN code (e.g. '7208 51 00' for Flat Hot-Rolled Steel)
- `imported_quantity_metric_tons` (float): Net weight of imported shipment in metric tonnes
- `actual_specific_embedded_emissions_tco2e_per_t` (float): Audited supplier plant emissions (tCO2e / t)
- `eu_default_benchmark_emissions_tco2e_per_t` (float): EU published conservative default value (tCO2e / t)
- `eu_ets_allowance_price_eur_per_tco2e` (float): Prevailing EU ETS carbon certificate price (EUR/tCO2e)

### Self-Test
```bash
python skills.py --test
```

### Model Context Protocol Integration (Claude Desktop / Cursor / Antigravity)
Add to your `mcpServers` configuration:
```json
{
  "mcpServers": {
    "genpark-agentic-commerce-cross-border-cbam-default-values-gap-auditor-skill": {
      "command": "python",
      "args": ["/path/to/genpark-agentic-commerce-cross-border-cbam-default-values-gap-auditor-skill/skills.py"]
    }
  }
}
```

## License
Licensed under Apache License 2.0. Copyright (c) 2026 GenPark Inc. (https://www.genpark.ai).
