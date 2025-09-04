# Entity-Graph Puzzle Game

## Vision
Create a browser-based puzzle game where each level presents a partially completed entity graph. ChatGPT generates the entities, relationships, and hints. Players drag node pieces from a side panel to the correct spots to complete the graph. The design follows KISS and the 80/20 rule: only essential features for a fun loop.

## MVP Features
- ChatGPT endpoint returns JSON describing fixed nodes, missing nodes, edges, and hints.
- React UI renders the graph and a container of draggable node pieces.
- Drag-and-drop placement with immediate validation and optional hint display.
- Simple score: correct placements divided by total nodes; "Next Puzzle" button loads a new level.

## Architecture
| Layer | Tech | Responsibility |
|-------|------|----------------|
| Frontend | React + lightweight graph lib (e.g., D3.js) | Render graph, drag-drop, local score |
| Backend | Node.js/Express | Request puzzle JSON from ChatGPT API and return to client |
| AI | ChatGPT | Generate puzzles and hints |

## User Flow
1. Landing page → "Play" loads a puzzle.
2. Drag nodes to fill empty slots; request hints if needed.
3. Upon completion show score/time and option for next puzzle.

## Roadmap
| Phase | Duration | Deliverables |
|-------|----------|-------------|
| Prototype | 2 wks | Wireframes, prompt format, sample puzzle |
| Core Build | 4 wks | Puzzle generator, interactive graph UI, scoring |
| Polish | 2 wks | Hint tweaks, responsiveness, basic analytics |

