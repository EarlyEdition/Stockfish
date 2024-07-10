<p align="center">
  <img src="https://github.com/Stockfish-NNUE/Stockfish-NNUE/assets/175236931/1134aea7-fdb5-4468-975f-c290152da37a" width="30%">
</p>

<h1 align="center">Stockfish NNUE</h1>

## Overview

Stockfish is a free, powerful UCI chess engine derived from Glaurung 2.1. It features two evaluation functions, the classical evaluation based on handcrafted terms, and the NNUE evaluation based on efficiently updateable neural networks. 

Stockfish is not a complete chess program and requires a UCI-compatible GUI (e.g. Cute Chess, Fritz, Arena, Sigma Chess, Shredder or Chess Partner) in order to be used comfortably.

## UCI parameters

Currently, Stockfish has the following UCI options:

  * #### Debug Log File
    Write all communication to and from the engine into a text file.

  * #### Contempt
    A positive value for contempt favors middle game positions and avoids draws.

  * #### Threads
    The number of CPU threads used for searching a position. For best performance, set
    this equal to the number of CPU cores available.

  * #### Hash
    The size of the hash table in MB.

  * #### Clear Hash
    Clear the hash table.

  * #### Ponder
    Let Stockfish ponder its next move while the opponent is thinking.

  * #### MultiPV
    Output the N best lines (principal variations, PVs) when searching.
    Leave at 1 for best performance.

  * #### Use NNUE
    Toggle between the NNUE and classical evaluation functions. If set to "true", the network parameters must be 
    availabe to load from file (see also EvalFile).

  * #### EvalFile
    The name of the file of the NNUE evaluation parameters. Depending on the GUI the filename might have to include 
    the full path to the folder/directory that contains the file.

  * #### Skill Level
    Lower the Skill Level in order to make Stockfish play weaker.

  * #### Move Overhead
    Assume a time delay of x ms due to network and GUI overheads. This is useful to
    avoid losses on time in those cases.

  * #### Minimum Thinking Time
    Search for at least x ms per move.

  * #### Slow Mover
    Lower values will make Stockfish take less time in games, higher values will
    make it think longer.

  * #### nodestime
    Tells the engine to use nodes searched instead of wall time to account for
    elapsed time. Useful for engine testing.

  * #### UCI_Chess960
    An option handled by your GUI. If true, Stockfish will play Chess960.

## Compiling Stockfish

The [MSYS2](https://www.msys2.org/) environment is recommended for compiling Stockfish on Windows.

To compile, type:

    make target ARCH=arch [COMP=comp]

Example: `make build ARCH=x86-64 COMP=mingw`

Lists of supported targets, archs and compilers can be viewed by typing `make help`.
