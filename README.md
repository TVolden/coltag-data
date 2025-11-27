# COLTAG Data
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17723526.svg)](https://doi.org/10.5281/zenodo.17723526)

Data was collected from participants play-testing a game procotype called [COLTAG](https://tvoldenitu.itch.io/coltag).

Participants could choose one or two emotions from: Engagement, frustration, boredom, confusion, and neutral.
Selected emotions were ordered alphabethecally and stored in seperate columns.

| Dataset | Data points |
| - | - |
| Clicks | 28660 |
| Events | 4078 |
| Interventions | 100 |
| MiniPXI | 32* |
| Sessions | 40 |
| Surveys | 747 |

## Clicks
Mouse events, mouse button pressed and released. Includes pixel coordinates.

| Field | Data type | Description |
| - | - | - |
| UserID | GUID | Unique ID persisted on client machine. |
| SessionID | GUID | Unique ID generated on game start. |
| Timestamp | Datetime | Local machine date time. |
| MouseX | Int | Pixel X-axis position on screen. |
| MouseY | Int | Pixel Y-axis position on screen. |
| ButtonIndex | Int | Mouse button index (left = 1, right = 2, wheel up = 4, wheel down = 5), [more info at godot](https://docs.godotengine.org/en/stable/classes/class_%40globalscope.html#enum-globalscope-mousebutton). |
| Action | String | Whether mouse button was pressed or released. |
| Utility | String | Item being dragged or "use" if no item is being dragged. |
| Hit | String | Identified asset being clicked or having item dropped on. |

## Events
Game events: Survey points, drag-and-drop interaction.

| Field | Data type | Description |
| - | - | - |
| UserID | GUID | Unique ID persisted on client machine. |
| SessionID | GUID | Unique ID generated on game start. |
| Timestamp | Datetime | Local machine date time. |
| Type | String | Event type (e.g. consent form). |
| Utility | String | Asset used (if any). | 
| Hit | String | Target asset (if any). |
| Result | String | Whether the event ended in a successful state change. |
| Description | String | A custom description of the event. |

## Interventions
Experimenter notes on interventions like hints and help given.

| Field | Data type | Description |
| - | - | - |
| UserID | GUID | Unique ID persisted on client machine. |
| SessionID | GUID | Unique ID generated on game start. |
| Timestamp | Datetime | Local machine date time. |
| Type | String | Intervention type (bug, help, hint). |
| Intervention | String | Description of the intervention. |

## MiniPXI
Results from MiniPXI including birth year and gender.

| Field | Data type | Description |
| - | - | - |
| UserID | GUID | Unique ID persisted on client machine. |
| SessionID | GUID | Unique ID generated on game start. |
| Timestamp | Datetime | Local machine date time. |
| BirthYear | Int | The birth year of the participant. |
| Gender | String | Gender of participant (Male, Female, \<none\>). |
| AUT | Int | Likert-scale -3 to 3. The Autonomy construct. |
| EC | Int | Likert-scale -3 to 3. The Ease of Control construct. |
| IMM | Int | Likert-scale -3 to 3. The Immersion construct. |
| PF | Int | Likert-scale -3 to 3. The Progress Feedback construct. |
| MAS | Int | Likert-scale -3 to 3. The Mastery construct. |
| MEA | Int | Likert-scale -3 to 3. The Meaning construct. |
| ENJ | Int | Likert-scale -3 to 3. The Enjoyment construct. |
| GR | Int | Likert-scale -3 to 3. The Clarity of Goals construct. |
| CH | Int | Likert-scale -3 to 3. The Challenge construct. |
| AA | Int | Likert-scale -3 to 3. The Audiovisual Appeal construct. |
| CUR | Int | Likert-scale -3 to 3. The Curiosity construct. |

## Sessions
Session meta data, start time, software version and last commit for prototype.

| Field | Data type | Description |
| - | - | - |
| UserID | GUID | Unique ID persisted on client machine. |
| SessionID | GUID | Unique ID generated on game start. |
| Timestamp | Datetime | Local machine date time. |
| Version | String | Software version (manually set) of the game. |
| Commit | String | Last recorded commit ID (git). |

## Surveys
Submitted survey points, featuring one or two emotions ordered alphabetically.

| Field | Data type | Description |
| - | - | - |
| UserID | GUID | Unique ID persisted on client machine. |
| SessionID | GUID | Unique ID generated on game start. |
| Timestamp | Datetime | Local machine date time. |
| Emotion1 | String | Selected emotion of two, no order (alphabetical). | 
| Emotion2 | String | Selected emotion if two were selected, no order (alphabetical). |