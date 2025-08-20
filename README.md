# CPM Node Playground

This repository provides a **Node Playground** for practicing Critical Path Method (CPM) exercises from chapter 5 of _Construction Project Scheduling and Control_ by Saleh Mubarak.

The tool combines a graphical network diagram with a data-entry table so you can practice creating activity networks and verifying your manual CPM calculations.

## Features

### Diagramming Area (Top Half)
- Add nodes to represent activities.
- Each node displays:
  - **Top row:** ES (Early Start), Activity Label, EF (Early Finish)
  - **Middle row:** Duration
  - **Bottom row:** LS (Late Start), TF (Total Float), LF (Late Finish)
- Drag nodes to arrange your network.
- Connect nodes with arrows to show dependencies. Arrowheads are filled triangles, outlined in white, and connect edge-to-edge for clarity.
- Delete selected nodes when needed.

### Table Area (Bottom Half)
- Serves as the main interface for entering CPM data.
- Columns include Activity, Duration, ES, EF, LS, LF, TF, Critical, and IPA (Immediately Preceding Activities).
- Node labels automatically update to reflect values entered in the table.

### Manual Calculation and "Check My Work"
- Enter all CPM values manually.
- The **Check My Work** button validates:
  - `EF = ES + Duration`
  - `LS = LF - Duration`
  - `TF = LF - EF`
  - `ES ≥ max(predecessor EF values)`
  - `LF ≤ min(successor LS values)`
  - Activities without predecessors typically have `ES = 0`
- Visual feedback:
  - Green highlighting for correct values
  - Red for errors
  - Yellow for warnings or values to review
  - Node borders mirror table feedback
- Mark activities as critical by entering "Yes" in the Critical column; critical activities are highlighted in gold.

## How to Use
1. Click **Add Activity** to create nodes.
2. Connect nodes to represent precedence relationships.
3. Enter activity names, durations, and CPM values directly in the table.
4. Click **Check My Work** to validate your calculations.
5. Review feedback and adjust values until all entries are correct.

This setup offers a hands-on environment for mastering CPM concepts and verifying manual calculations without automatically solving the schedule for you.
