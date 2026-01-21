## Webview Error: "Could not register service worker" or "InvalidStateError"

### Description
The error "Error loading webview: Error: Could not register service worker: InvalidStateError: Failed to register a ServiceWorker: The document is in an invalid state.." appears to occur intermittently when visualizing rules or using webviews. 

This is caused by corrupted Electron cache or hung background processes.

### Solution
   - Force kill all Antigravity processes (`pkill -9`).
   - Clear `Service Worker`, `Cache`, `blob_storage`, and other ephemeral directories in `~/.config/Antigravity/`.
   - Restart Antigravity

**Fallback:** If the this doesn't resolve the issue, performing a full system reboot to clear shared memory segments.
