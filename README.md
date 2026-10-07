# CasaBella Outdoor Kitchen & Built-In Grill Designer (MCP server)

Find the right built-in grill and plan the outdoor kitchen around it: real MSRP for grills and
cabinets, a priced starter layout, every layout explained, a free photoreal 3D render and a formal
quote from a local dealer.

- **Server URL:** `https://www.casabellaoutdoor.com/api/mcp`
- **Transport:** Streamable HTTP (MCP 2026-07-28, with 2025 clients supported)
- **Authentication:** none
- **Registry name:** `com.casabellaoutdoor/outdoor-kitchen`
- **Docs for AI assistants:** https://www.casabellaoutdoor.com/ai/
- **Publisher:** [CasaBella Outdoor](https://www.casabellaoutdoor.com)

This is a hosted server run by CasaBella Outdoor. There is nothing to install or run locally;
this repository documents how to connect to it.

## Connect

| App | How |
|---|---|
| Claude (claude.ai, desktop, mobile) | Customize → Connectors → Add custom connector → paste the server URL |
| ChatGPT | Add a custom connector / app with the server URL (developer mode on supported plans) |
| Grok | grok.com/connectors → New Connector → Custom → paste the server URL |
| Perplexity, Mistral Le Chat | Add a custom remote MCP connector with the server URL |
| Any MCP client | Remote server, Streamable HTTP, the URL above, no auth |

## Tools

| Tool | What it does |
|---|---|
| `outdoor_kitchen_start_planning` | Guided start: grill options with MSRP, then a priced starter layout from a few questions |
| `outdoor_kitchen_search_built_in_grills` | Built-in grills by brand, size and MSRP, with the grill cabinet each needs |
| `outdoor_kitchen_list_grill_brands` | Grill brands available in the designer |
| `outdoor_kitchen_list_cabinets` | Cabinet types and sizes with MSRP |
| `outdoor_kitchen_list_layouts` | Straight, galley, Corner L, Corner 45, U-Shape, Promenade |
| `outdoor_kitchen_price_design` | MSRP for a straight island: cabinetry only, + grill & appliances, + countertop area |
| `outdoor_kitchen_get_suggestions` | Suggestions, only when the shopper asks (e.g. how to lower the cost) |
| `outdoor_kitchen_open_designer_for_render` | Opens the 3D designer; free photoreal render by email |
| `outdoor_kitchen_request_formal_quote` | Formal quote; a local dealer follows up |

Every result includes a `next` field with the recommended next step.

## Example prompts

- "I'm shopping for a 36-inch built-in grill. What are my options and what do they cost?"
- "Plan a 10-foot outdoor kitchen with a built-in grill, a refrigerator and a sink. Roughly what would it cost?"
- "What outdoor kitchen layouts are there? I want bar seating."
- "How could I lower the cost?"
- "I'd like a 3D render of this layout."

See [`examples/`](examples/) for sample tool calls.

## Pricing

Prices are MSRP and are labeled by what they include: cabinetry only; cabinetry plus grill and
appliances; and a countertop area with a typical installed estimate. Installation, gas and
electrical are extra. Final pricing is determined by your local dealer.

## Privacy

Browsing grills, layouts and prices needs no personal information. A render or quote needs a name
and email (ZIP optional, to find a local dealer). Returning shoppers confirm a 6-digit code sent to
their email before a saved design opens. Privacy policy: https://www.casabellaoutdoor.com/privacy-policy

## Support

sales@casabellaoutdoor.com
