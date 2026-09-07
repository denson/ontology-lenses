# Ontology lenses: a guide for people and AI assistants

This is the Markdown companion to [Ontology lenses](https://denson.github.io/ontology-lenses/), an interactive illustration of viewing connected knowledge through multiple lenses. Share this document's URL with an AI assistant to discuss the ideas behind the visualization.

Document URL: https://denson.github.io/ontology-lenses/guide.md

Source: https://github.com/denson/ontology-lenses

Updated: 2026-09-06

## What the site represents

The same things can participate in several kinds of relationships. A person can belong to a category, perform an activity, and be associated with a supporting record. Changing the question brings different relationships into view while preserving the identity of the things being discussed.

The artwork contains 25 networks in a three-dimensional arrangement and 4,371 persistent synthetic entities. Its central cluster is three times its original size. Positions, sizes, and connections are procedural design choices. They are not measurements of importance, confidence, similarity, or real-world distance.

This is a conceptual demonstration. Structure, Activity, and Evidence are the demonstration's three illustrative lenses. The site does not load a production knowledge graph or formally defined domain ontologies. The example below supplies names and facts for explanation; those records are not loaded into the animated scene.

## Vocabulary

| Term | Meaning in this guide |
| --- | --- |
| Entity / node | A particular thing, such as a person, device, event, or report. |
| Entity type | A category that describes what kind of thing an entity is. |
| Relationship / edge | A connection with a meaning, such as a test **uses** a sensor. |
| Ontology | A vocabulary of types and relationships, with definitions and rules for interpreting them. |
| Lens | A question-focused view that emphasizes certain entity types and relationships. A lens is a view over knowledge; the three buttons illustrate possible views. |
| Network / cluster | A visual grouping of connected nodes. The 25 clusters are not 25 identified real ontologies. |
| Shared anchor | A persistent visual reference that helps you recognize the same structure across lens changes. |
| Ontology mapping | An explicit correspondence between concepts or relationships expressed in different vocabularies. The artwork uses dashed connections to illustrate this idea. |

## How to read the visual

| Mark | Meaning |
| --- | --- |
| Blue circle: Actor | A person, team, organization, or other participant. |
| Green square: Asset | A resource, device, material, or other thing used in an activity. |
| Orange diamond: Activity | Something that happens or is done. |
| Purple triangle: Evidence | A record, observation, or source that documents or supports something. |
| Ringed anchor | A reference point that persists across lenses. |
| Solid connection | A relationship within a network. |
| Dashed connection | An illustrative mapping between networks. |

Colors and shapes retain their meaning when you change lenses. Dim nodes still exist. Brightness reflects visual emphasis, depth, and the animated pulse; it is not a numerical confidence score. Rings do not indicate independently verified identity matches.

## What each lens asks

| Lens | Question | What changes on the page |
| --- | --- | --- |
| Structure | What kinds of things are here? | Blue actors and green assets stand out, with classification and grouping relationships. |
| Activity | Who does what, using which resources? | Orange activities and their participant/resource relationships stand out. |
| Evidence | What documents or supports this? | Purple evidence and its supporting relationships stand out. |

The entities keep their identities and local positions. The visible relationship set and emphasis change. Tapping a lens pauses motion so that you can compare the same pose; **Auto** resumes rotation and cycling, subject to reduced-motion settings.

## A concrete example: one test, three views

Consider these fictional records:

| Stable ID | Name | Type |
| --- | --- | --- |
| `actor:mira` | Mira | Actor |
| `asset:sensor7` | Sensor 7 | Asset |
| `activity:test42` | Test 42 | Activity |
| `evidence:report42` | Report 42 | Evidence |

The example contains three stated relationships:

```text
activity:test42 --performedBy--> actor:mira
activity:test42 --usesAsset----> asset:sensor7
evidence:report42 --documents-> activity:test42
```

Read a pair of connected things together with the relationship between them. `Test 42 --usesAsset--> Sensor 7` means that Test 42 uses Sensor 7. It does not say that the test and the sensor are the same thing. A pair of endpoints alone cannot tell you what a connection means. The artwork's lines are illustrative and do not expose individual predicate labels.

- **Structure view:** Mira is an actor; Sensor 7 is an asset; Test 42 is an activity; Report 42 is evidence. These are classifications of the same four records.
- **Activity view:** Test 42 was performed by Mira and used Sensor 7. This answers who participated and what resource was involved.
- **Evidence view:** Report 42 documents Test 42. This supplies a record to inspect when asking about the test. The existence of a report alone does not establish that the test succeeded or that its conclusions are correct.

An example question spanning the views is: **Who performed Test 42, what did they use, and what record documents it?**

From the stated example facts: **Mira performed Test 42 using Sensor 7, and Report 42 documents the test.** Each part of that answer follows a named relationship. Test results, dates, and the reliability of Report 42 are unspecified.

## What a mapping adds

Imagine that a lab vocabulary calls a device an **Instrument**, while an inventory vocabulary uses the broader category **Asset**. A mapping can state that every Instrument in this example counts as an Asset. The reverse need not hold: an Asset could also be a building or a material.

That is a correspondence between categories. Identifying two records as the same specific device is a separate claim. A lab's `instrument:S7` and an inventory system's `asset:481` would need an explicit identity link supported by identifying information, such as a verified shared serial number. Similar labels alone do not establish identity.

Mappings allow a question expressed in one vocabulary to reach relevant knowledge expressed in another while retaining those distinctions. The demonstration's dashed lines do not distinguish exact, approximate, or broader/narrower correspondences, and they do not implement a mapping reasoner.

## What Send a query does

**Send a query** restarts a timed wave of light through the nodes and connections, including connections between clusters. It illustrates following relationships across the networks. It also runs while rotation is paused.

The button is an animation control. It accepts no question text, executes no semantic query, and returns no retrieved answer. There is no AI model or query service behind the page. The fictional answer above comes from this document's stated facts, not from running the button.

**Play/Pause** controls motion. Dragging orbits the scene; a mouse wheel or two-finger pinch zooms from 0.6x to 5x. Zoom is retained when you change lenses.

## A prompt to share with your AI

Copy this prompt along with the guide URL:

> Read https://denson.github.io/ontology-lenses/guide.md and explain how Structure, Activity, and Evidence offer different views of the same entities. Walk me through the Mira / Sensor 7 / Test 42 / Report 42 example. Explain the difference between a relationship, a mapping between categories, and a claim that two records identify the same object. Then help me sketch an example from my own domain, separating the facts I provide from assumptions and information we would still need.

An assistant that cannot open links can work from the Markdown pasted into the conversation. The guide is public context to share with an assistant; opening the site does not automatically provide it to a separate AI service.
