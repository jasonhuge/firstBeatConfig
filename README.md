# FirstBeat Configuration

Configuration files for the FirstBeat improv app. This repository contains JSON data for improv formats, warmup exercises, and opening techniques used in improvised theater performances.

## Overview

FirstBeat is an improvisation app that helps performers structure and manage improv shows. This repository serves as the central configuration store for:

- Long-form improv formats and their structures
- Warmup exercises organized by category
- Opening techniques with player counts and timing

## Repository Structure

```
json/
├── formats.json    # Long-form improv format definitions
├── warmups.json    # Warmup exercises and games
└── openings.json   # Show opening techniques
```

## Configuration Files

### formats.json

Contains long-form improv format definitions including:

- **Harold** - A foundational long-form structure with repeated scene beats, thematic exploration, and ensemble group games
- **Montage** - A flexible format of independent scenes connected by theme, tone, or idea
- **Pretty Flower** - A pattern-based format alternating between two-person scenes and group games
- **The Hulk** - A character-driven format that escalates from grounded reality to extreme absurdity
- **Armando** - A narrative format inspired by personal monologues

Each format includes:
- Description and structure
- Preferred and allowed opening techniques
- Segments with time portions
- Unique identifiers for cross-referencing

### warmups.json

Contains improv warmup exercises organized into four categories:

- **Physical** - Body-based exercises (Zip Zap Zop, Mirror Exercise, Crazy Eights, etc.)
- **Vocal** - Voice and sound exercises (Sound Ball, Gibberish, Tongue Twisters, etc.)
- **Mental** - Quick-thinking and focus games (Word Association, Five Things, Status Exercise, etc.)
- **Group** - Ensemble-building activities (Hot Spot, Yes And Circle, Big Booty, etc.)

Each warmup includes:
- Description and how to play
- Variations for different skill levels
- Tips for facilitators
- Category classification

### openings.json

Contains opening techniques for improv shows:

- **Organic Opening** - Ensemble-driven free-form exploration
- **Monologue** - Solo personal storytelling
- **Invocation** - Group word association
- **Living Room** - Conversational discussion
- **Pattern Game** - Repeating verbal/physical patterns
- And more...

Each opening includes:
- Description and purpose
- Player count requirements
- Expected setup time
- Unique identifier for linking with formats

## Data Structure

All files use standard JSON format with consistent schemas:

**Format Schema:**
```json
{
  "id": "string",
  "title": "string",
  "name": "string",
  "description": "string",
  "preferred_opening_id": "string",
  "allowed_opening_ids": ["string"],
  "segments": [
    {
      "title": "string",
      "portion": number
    }
  ]
}
```

**Warmup Schema:**
```json
{
  "name": "string",
  "category": "Physical|Vocal|Mental|Group",
  "description": "string",
  "howToPlay": "string",
  "variations": ["string"],
  "tips": ["string"]
}
```

**Opening Schema:**
```json
{
  "id": "string",
  "name": "string",
  "description": "string",
  "player_count": "string",
  "setup_time": "string"
}
```

## Usage

These configuration files are designed to be consumed by the FirstBeat improv app. The JSON data provides:

- Structured show formats for performers to follow
- Searchable warmup library for instructors and coaches
- Opening techniques matched to appropriate formats via ID references

## Contributing

When adding or modifying configuration data:

1. Maintain consistent JSON structure
2. Validate JSON syntax before committing
3. Use clear, descriptive text appropriate for performers
4. Ensure opening IDs referenced in formats exist in openings.json
5. Keep descriptions concise but informative

## License

Configuration data for the FirstBeat improv application.