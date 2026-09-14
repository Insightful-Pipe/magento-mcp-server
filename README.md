# Magento MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/magento)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect Magento to AI assistants: products, orders, inventory and sales for Magento 2 and Adobe Commerce.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — use Magento from Claude, ChatGPT, Cursor, and other AI assistants through the Model Context Protocol (MCP).

<img src="images/magento-icon.svg" alt="Magento MCP Server" width="64" height="64">

## MCP Server URL

```
https://magento.insightfulmcp.com/
```

## What is Magento MCP?

Magento MCP is a **remote Model Context Protocol server** hosted by InsightfulPipe. Access products, orders, customers, inventory, and categories from your Magento 2 or Adobe Commerce store.

## Installation

### Claude

1. Copy the MCP Server URL: `https://magento.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** on the connector to start authorization
6. Click **Authorize access** in the browser to complete the connection

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://magento.insightfulmcp.com/`
3. Authorize with your InsightfulPipe account

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http magento https://magento.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "magento": {
      "url": "https://magento.insightfulmcp.com/"
    }
  }
}
```

Then authorize the connection when Cursor prompts you.

## Available Actions

37 actions: 25 read, 12 write.

### Read Actions (25)

| Action | Description |
|--------|-------------|
| `get_category` | Get a specific category by ID |
| `get_category_tree` | Get the full category tree |
| `get_cms_block` | Get a specific CMS block by ID |
| `get_cms_page` | Get a specific CMS page by ID |
| `get_invoice` | Get a specific invoice by ID |
| `get_order` | Get a specific order by ID |
| `get_order_count` | Get the number of orders for a date range |
| `get_product` | Get a specific product by SKU |
| `get_product_sales` | Get product sales statistics for a date range |
| `get_revenue` | Get total revenue for a date range |
| `get_revenue_by_country` | Get revenue filtered by country for a date range |
| `get_stock_item` | Get stock item details for a product SKU |
| `get_stock_status` | Get stock status for a product SKU |
| `get_store_config` | Get store configuration |
| `get_store_groups` | Get store groups |
| `get_store_views` | Get store views |
| `get_websites` | Get websites |
| `search_categories` | Search categories with filters and pagination |
| `search_cms_blocks` | Search CMS blocks with filters and pagination |
| `search_cms_pages` | Search CMS pages (articles) with filters and pagination |
| `search_credit_memos` | Search credit memos with filters and pagination |
| `search_invoices` | Search invoices with filters and pagination |
| `search_orders` | Search orders with filters and pagination |
| `search_products` | Search products with filters and pagination |
| `search_shipments` | Search shipments with filters and pagination |

### Write Actions (12)

| Action | Description |
|--------|-------------|
| `create_category` | Create a new category |
| `create_cms_block` | Create a CMS block |
| `create_cms_page` | Create a CMS page |
| `create_product` | Create a new product |
| `delete_category` | Delete a category by ID |
| `delete_cms_block` | Delete a CMS block by ID |
| `delete_cms_page` | Delete a CMS page by ID |
| `delete_product` | Delete a product by SKU |
| `update_category` | Update an existing category |
| `update_cms_block` | Update a CMS block |
| `update_cms_page` | Update a CMS page |
| `update_product` | Update an existing product by SKU |

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

```
"What was my revenue by country last month?"
```

```
"Which products are out of stock?"
```

```
"Show orders placed in the last 7 days"
```

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers.

- [Shopify MCP](https://insightfulpipe.com/mcp-servers/shopify)
- [WooCommerce MCP](https://insightfulpipe.com/mcp-servers/woocommerce)
- [Google Merchant Center MCP](https://insightfulpipe.com/mcp-servers/google-merchant-center)

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-magento)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
