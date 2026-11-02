# Server MCPS2

## 1. Overview
This is an MCP server developed in Python using uv that leverages the official MCP Python SDK (https://github.com/modelcontextprotocol/python-sdk) as the context manager for agents. It features asynchronous communication via kafka-python with other servers to adapt and serve real-time context information. Furthermore, it integrates pytest and testcontainers for robust testing support.

### Main objectives:
- Develop the MCP server under a hexagonal architecture (focused on tools and resources).
- Allow dynamic updating of context content, which in turn influences agent responses (update commands originate from a logic management server, not part of this repository).
- Provide auditing capabilities for agents querying the server to report usage metrics to another management server (the logic manager is OUTSIDE this repository).
- Establish a resilient and adaptable structure for dynamic contexts (e.g., programmatic converters, dependency injection, low coupling, etc).

## 2. Technologies
Python (3.14.4)
uv (0.12.1)
MCP (2.3.0)
kafka-python (3.0.12)
pytest (9.2.0)
testcontainers (4.15.0)
