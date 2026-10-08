# AlbertoPlayer (CSHARPGUI) — Presentation Layer & Desktop UI

[![.NET](https://img.shields.io/badge/.NET-Desktop%20WPF-512BD4?logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Language](https://img.shields.io/badge/Language-C%23%20%2F%20XAML-239120?logo=csharp&logoColor=white)](https://docs.microsoft.com/dotnet/csharp/)
[![Architecture](https://img.shields.io/badge/Architecture-Presentation%20Layer%20(GUI)-orange)](#system-architecture)
[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows&logoColor=white)](https://microsoft.com)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

The front-facing Graphical User Interface (GUI) desktop client for the modular C# music player suite. Delivers an interactive user experience with responsive media controls, track queue visualization, and seamless integration with core playback logic and database services.

---

## 🌐 Language / Język
- [🇬🇧 English](#-english-version)
- [🇵🇱 Polski](#-wersja-polska)

---

## 🇬🇧 English Version

### About the Project
**AlbertoPlayer** (`CSHARPGUI`) is the **Presentation Layer** of a modular .NET audio player system. Built using **C#** and **WPF (Windows Presentation Foundation)** with declarative **XAML**, the application translates user inputs into commands processed by the backend engine while rendering rich UI components such as playback timelines, volume controls, and database-backed playlists.

### System Architecture
AlbertoPlayer sits at the top of the 3-tier modular architecture:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   AlbertoPlayer / CSHARPGUI (This Project)             │
│     • XAML UI Views & Custom Controls                                  │
│     • Playback Controls (Play, Pause, Seek, Volume)                    │
│     • Data Binding & Event Triggers                                    │
└──────────────────────────────────┬─────────────────────────────────────┘
                                   │ Invokes engine commands & state
                                   ▼
       ┌────────────────────────────────────────────────────────┐
       │     Core Logic Engine: csharp-musicplayer              │
       │     (Queue Management, Track Entities, State Machine)  │
       └───────────────────────────┬────────────────────────────┘
                                   │ Queries persistent storage
                                   ▼
       ┌────────────────────────────────────────────────────────┐
       │     Persistence Layer: sqlwpf (SQL Database Access)    │
       └────────────────────────────────────────────────────────┘
