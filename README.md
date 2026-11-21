# Getting started with ADK, MCP and A2A

Materials for a 30-minute live session on building agents with Google's [Agent Development Kit](https://adk.dev/), sharing tools with the [Model Context Protocol](https://modelcontextprotocol.io/), and connecting agents with the [Agent2Agent protocol](https://a2a-protocol.org/).

- **Session page:** [index.html](https://tahreemrasul.github.io/adk-mcp-a2a-session/) covers tools, function calling, agents, ADK, MCP and A2A, with links to the notebook part for each section.
- **Notebook:** [Open in Colab](https://colab.research.google.com/github/tahreemrasul/adk-mcp-a2a-session/blob/main/notebook.ipynb). One currency-conversion function goes from a plain function call, to an ADK agent tool, to an MCP server, to an agent that another agent calls over A2A.

## Running the notebook

You need a free Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey). In Colab, add it as a secret named `GOOGLE_API_KEY` (key icon in the left sidebar).

To run it locally instead, use Python 3.10+ and:

```bash
pip install "google-adk[a2a]==2.15.0" "mcp==2.3.0" "uvicorn==0.54.0" jupyter
export GOOGLE_API_KEY=<your-key>
jupyter notebook notebook.ipynb
```

Tested with google-adk 2.15, mcp 2.3 and a2a-sdk 1.3. In `mcp` 2.x, `FastMCP` was renamed to `MCPServer`, so older tutorials that import `FastMCP` will fail with these versions.
