<p align="center">
  <img src="logo.png" width="88" alt="Systra Tools">
</p>

<h1 align="center">Systra Tools</h1>

<p align="center">
  A growing collection of production-ready React + Tailwind sections and elements,<br>
  searchable by your coding agent over MCP.
</p>

<p align="center">
  <a href="cursor://anysphere.cursor-deeplink/mcp/install?name=systra-tools&config=eyJ1cmwiOiJodHRwczovL3N5c3RyYS50b29scy9hcGkvbWNwIiwiaGVhZGVycyI6eyJBdXRob3JpemF0aW9uIjoiQmVhcmVyICR7ZW52OlNZU1RSQV9NQ1BfS0VZfSJ9fQ=="><img src="https://cursor.com/deeplink/mcp-install-dark.png" alt="Add systra-tools to Cursor" height="32"></a>
</p>

<p align="center">
  <a href="https://lobehub.com/mcp/roesmannamelie-alt-systra-tools-plugin"><img src="https://lobehub.com/badge/mcp/roesmannamelie-alt-systra-tools-plugin" alt="MCP Badge"></a>
</p>

---

Systra Tools is a growing library of React and Tailwind sections and elements:
heroes, pricing tables, bento grids, dashboards, footers and more. This
repository connects it to your coding agent over MCP, so Claude, Cursor or
VS Code can search the library and drop a section into your project as a
single TSX file.

Every component imports only react, framer-motion and lucide-react and
respects reduced motion. Free components are available without a key. A Premium key from https://systra.tools/mcp opens the whole library, the
image library and the page recipes.

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

### VS Code, Windsurf and anything else that speaks MCP

Point an HTTP MCP server at `https://systra.tools/api/mcp` and send your key
as `Authorization: Bearer <key>`.

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

The key is optional. Without one the agent gets the free sample components.
For the full library, create a Premium key at
[systra.tools/mcp](https://systra.tools/mcp) and put it in the environment as
`SYSTRA_MCP_KEY`. Do not commit the key.

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

## What is in this repository

A rule, two skills and the MCP configuration. That is all a plugin is. The
component library itself lives behind the MCP server.

## License

The configuration in this repository is MIT licensed. The components you
pull through the MCP server are licensed separately, see
https://systra.tools/terms.
