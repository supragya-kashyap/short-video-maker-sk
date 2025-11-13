import { createRequire } from "module";
const require = createRequire(import.meta.url);
const _ES = require("eventsource");
const EventSource = _ES && (_ES.default || _ES.EventSource) ? (_ES.default || _ES.EventSource) : _ES;

const SSE_URL = "http://short-video-maker-main-short-creator-1:3123/mcp/sse";
console.log("Connecting to MCP SSE:", SSE_URL);
const es = new EventSource(SSE_URL);

es.onopen = () => console.log("✅ MCP SSE connected");
es.onmessage = (e) => console.log("📩 Message:", e.data);
es.onerror = (e) => console.error("❌ SSE error:", e && e.message ? e.message : e);
