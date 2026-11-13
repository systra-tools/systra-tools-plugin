# Systra Tools

A growing collection of production-ready React + Tailwind sections and
elements, searchable by your coding agent over MCP.

[![Add systra-tools to Cursor](https://cursor.com/deeplink/mcp-install-dark.png)](cursor://anysphere.cursor-deeplink/mcp/install?name=systra-tools&config=eyJ1cmwiOiJodHRwczovL3N5c3RyYS50b29scy9hcGkvbWNwIiwiaGVhZGVycyI6eyJBdXRob3JpemF0aW9uIjoiQmVhcmVyICR7ZW52OlNZU1RSQV9NQ1BfS0VZfSJ9fQ==)
[![Add to Replit](https://replit.com/badge?caption=Add%20to%20Replit)](https://replit.com/integrations?mcp=eyJkaXNwbGF5TmFtZSI6IlN5c3RyYSBUb29scyIsImJhc2VVcmwiOiJodHRwczovL3N5c3RyYS50b29scy9hcGkvbWNwIn0=)
[![MCP Badge](https://lobehub.com/badge/mcp/systra-tools-systra-tools-plugin)](https://lobehub.com/mcp/systra-tools-systra-tools-plugin)

---

Systra Tools is a growing library of React and Tailwind sections and elements:
heroes, pricing tables, bento grids, dashboards, footers and more. This
repository connects it to your coding agent over MCP, so Claude, Cursor or
VS Code can search the library and drop a section into your project as a
single TSX file.

Every component imports only react, framer-motion and lucide-react and
respects reduced motion.

The first six components in each category are free without an account or key.
Premium unlocks the complete source library and additional media. In Claude,
Premium can use your Systra account sign-in; in coding editors you can use a
personal MCP key from https://systra.tools/mcp.

## Install

### Cursor

Click the button above, or add the plugin from
[cursor.directory](https://cursor.directory), or configure it by hand in
`~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "systra-tools": {
      "url": "https://systra.tools/api/mcp",
      "headers": { "Authorization": "Bearer ${env:SYSTRA_MCP_KEY}" }
    }
  }
}
```

### Claude Code

```
/plugin marketplace add systra-tools/systra-tools-plugin
/plugin install systra-tools@systra
```

### Lovable, Bolt, v0 and Replit

- **Lovable:** Connectors, then the Custom MCP card at the bottom. Paste
  `https://systra.tools/api/mcp` and click Add server.
- **Bolt:** Connectors (MCP), then Custom MCP server. Transport HTTP,
  authentication None, or API key for Premium.
- **v0:** Add MCP under MCP Connections or in the prompt field. No Auth, or
  Bearer Token with your Premium key.
- **Replit:** click the Add to Replit button above, or Integrations, MCP, Add
  MCP server with the same address.

### VS Code, Windsurf and anything else that speaks MCP

Point an HTTP MCP server at `https://systra.tools/api/mcp`. That alone works
for the free components; with a Premium key, send it as
`Authorization: Bearer <key>`.

## Your first result with Systra Tools

Once connected, paste this directly into Claude Code or another MCP-enabled
coding agent with access to your React project:

> Build a modern SaaS landing page in my React project using free Systra Tools sections. Find a hero, features, pricing and CTA with the Systra Tools MCP tools. Fetch the real TSX source, integrate it with Tailwind, and make the page responsive. If a section needs Premium, show a free alternative.

For a smaller first step:

> Find a free Systra Tools hero section, explain the design and add its TSX source to my React project.

In Claude web chat without local file access, Claude can find and display
components, but cannot directly edit the files on your computer.

## Improve the design, not just the code

The MCP server gives your coding agent real UI components. The separate, free
[Systra Taste skills](https://github.com/systra-tools/systra-taste) help it
decide **which** composition works, review generic layouts, and preview distinct
redesigns before replacing an existing interface.

```bash
npx skills@latest add systra-tools/systra-taste
```

Use `systra-taste` to build, `systra-taste-review` to critique, and
`systra-taste-repair` to redesign. They work without a key; this MCP integration
is optional.

## Your key

The key is optional. Without one, the agent can browse the full catalog and
retrieve source for the first six components of each category. To unlock the
full library in coding editors, create a Premium key at
[systra.tools/mcp](https://systra.tools/mcp) and set `SYSTRA_MCP_KEY`.
Never commit your key. In Claude's connector you can sign in to your Systra
account instead.

## What the agent gets

| Tool | What it does |
| --- | --- |
| `list_categories` | categories with counts |
| `list_components`, `search_components` | find a section by intent |
| `get_component` | the full source |
| `list_recipes`, `get_recipe` | an ordered page recipe |
| `list_styles`, `get_style`, `get_component_styled` | the same component in a real brand's colours and fonts |
| `list_images`, `search_images` | imagery with permanent URLs |
| `list_posts`, `get_post` | social post templates |

Prompts: `build_landing_page`, `find_section` and `restyle_component` run the
usual workflows as a single command. Resources: `systra://catalog/categories`
and `systra://catalog/recipes` list the catalog without a tool call. Both work
without a key.

## What is in this repository

A rule, two skills and the MCP configuration. That is all a plugin is. The
component library itself lives behind the MCP server.

## License

The configuration in this repository is MIT licensed. The components you
pull through the MCP server are licensed separately, see
https://systra.tools/terms.
