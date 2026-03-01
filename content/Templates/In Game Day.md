<%*
// Path to your counter note (adjust this to match your location)
const counterNote = "Launch";

// Get the counter note file
const file = tp.file.find_tfile(counterNote);

// Read current counter value from frontmatter
const fileCache = app.metadataCache.getFileCache(file);
let counter = fileCache?.frontmatter?.daysInGame || 0;

// Increment counter
counter++;

// Read the full file content
let content = await app.vault.read(file);

// Update the frontmatter with new counter value
content = content.replace(/daysInGame:\s*\d+/, `daysInGame: ${counter}`);

// Write back to file
await app.vault.modify(file, content);

// Output the template with the new counter value
tR += `\n### Day ${counter}\n---\n- `;
%>