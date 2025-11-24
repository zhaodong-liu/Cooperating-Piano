## Cooperating Piano
This project is a virtual piano application that supports **real-time multi-user collaboration**, **music recording/playback**, and **customizable sound generation**.
Developed as the final project for **CS-UY 3913 Java and Web Design**.

## Features
- Emulated piano keyboard with notes from C4 to C7
- One real sampled piano sound pack and 4 electronic sounds (sine, square, triangle, sawtooth)
- Simple chord generator
- Real-time multi-user collaboration via TCP networking
- Text chat system for communication between users
- Record and save music in a simple text format
- Play music from local files
- Visual metronome with animated pendulum

## Project Structure
```
Cooperating-Piano/
├── src/
│   └── main/
│       ├── java/com/cooperatingpiano/    # Java source files
│       └── resources/audio/              # Audio resources
│           └── piano_samples/            # Piano WAV samples
├── docs/                                 # Documentation
│   ├── project-report/                   # Academic project report
│   └── user-guide/                       # User guide
├── examples/                             # Example music recordings
├── .gitignore                            # Git ignore rules
└── README.md                             # This file
```

## Building and Running

### Compilation
```bash
# Compile all Java files
javac -d bin -sourcepath src/main/java src/main/java/com/cooperatingpiano/*.java

# Or compile with resources
javac -cp src/main/resources -d bin -sourcepath src/main/java src/main/java/com/cooperatingpiano/*.java
```

### Running the Application
```bash
# Run the client application (macOS/Linux)
java -cp bin:src/main/resources com.cooperatingpiano.PianoApp

# Run the client application (Windows)
java -cp bin;src/main/resources com.cooperatingpiano.PianoApp

# Run the server (for multi-user collaboration)
java -cp bin com.cooperatingpiano.PianoServer
```

**Note:** The application will try to load audio samples from:
1. Classpath resources (when packaged)
2. `src/main/resources/audio/piano_samples/` (development mode)
3. `piano_samples/` (legacy compatibility)

## Requirements
- Java 21 or later
- Audio samples are included in `src/main/resources/audio/piano_samples/`

## Documentation
- [Project Report](docs/project-report/ProjectReport.pdf) - Detailed academic project report
- [User Guide](docs/user-guide/Cooperating-Piano-User-Guide.pdf) - End-user documentation

## Example Recordings
Sample music recordings are available in the `examples/` directory:
- `mozart-k525.txt` - Mozart's Eine kleine Nachtmusik excerpt
- `charli-xcx-360.txt` - Charli XCX 360 arrangement
