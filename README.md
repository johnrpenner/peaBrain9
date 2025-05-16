peaBrain 9 ©2025 by John Roland Penner
peaBrain 9 is a UCI Chess Engine written in Swift for macOS
version 9.0.5 released: May 15, 2025

peaBrain 9 is the UCI version of the engine used in my commercial Chess Meister product for the iPhone. it provides a simple pedagogical chess engine written in Swift which should be easily comprehensible to anyone interested in getting started with chess programming. It can be played in any UCI compatible Chess GUI application like HIARCS. 

peaBrain uses a classic Shannon type MiniMax search with Quiescence extensions and Alpha-Beta pruning, SAN Notation, and is written to support Fischer games (pending), The opening book includes 10,000 moves from the ECO (Encyclopedia of Chess Openings). Runs at about 1900 ELO within Time Controls. Comes complete with Swift source code. 

peaBrain is the Slowest Engine out there — but at least i wrote the moveGenerator on my own without ripping someone else's Bitboard like the Stockfish clones. The entire codebase is a functional port of an earlier chess engine i had written in 2010 in futureBasic called pChess 2.0 — and peaBrain 9 finally matches its use of hash tables for greater speed, and support for fischer random chess (pending). pChess 2.0 came with a graphical interface which allowed sound and graphic visualization of the moves in real-time as they were being processed by negamax as part of an iMac art installation. After 15 years, I have partially reiplemented the AudioBrain and VisualBrain in a new peaBoard UCI GUI for macOS (please contact me if you wish to be a beta tester for the new GUI). 

Advancements of peaBrain 9 over peaBrain 8 are: Multi-Core Processor Support, a reiplementation of Zobrist Hash Tables from pChess 2.0, and the addition of PV (principal variation) Search which is now reported through UCI info. 

peaBrain 9.0.5 also fixes a UCI position bug — where it would revert to a white who2move after being provided a FEN with black to move, and then the engine would stall. this has been fixed. the bug was in the UCI handler, and not the engine itself — whole logic remains stable, but I need to rerun it through the EPD tests for evaluation integrity. 


Usage: compile this puppy with: 

	swiftc -o pea9 peaBrain9.swift -Ounchecked -suppress-warnings 

and see if you can beat the peabrain! 🤩 

NOTE: you NEEED to use -Ounchecked for 100x the SPEEED!! 
	PERFT on M1 with -Ounchecked = depth 5 nodes 4865609✅ time 3.31 nps 1468141.10
	PERFT on M1 without -Ounchecked depth 5 nodes 4865609✅ time 917.09 nps 5305.47


john roland penner
toronto island 🇨🇦 


--| HISTORY peaBrain 1-9 |-----

Development Timeline: 
• 2009 - pChess 1.0 
• 2010 - pChess 2.0; dropFour 
• 2011 - pChess UCI; port to C++ 
• 2012 - pea3.4 C++ commandline; [freeSpace] 
• 2013 - peaBrain 4.3 C++ engine 
• 2014 - Chess Meister 1.0 
• 2015 - NEX4 1.0; [OMM elisa clone] 
• 2016 - Music Invaders 1.0 
• 2016 - peaBrain5 Swift Chess Engine 
• 2017 - Chess Meister II for iPhone 
• 2018 - Hnefatafl 0.9.0 
• 2021 - pea3 C++ commandline > GitHub 
• 2023 pseudoEngine UCI 
• 2024 peaBrain 8 UCI > GitHub
• 2025 peaBrain 9 UCI > GitHub  // add multithreading + hash


--| THANKS |------------------------------------------------

• Papa Penner Sr. for Games of Real Chess.
• Robert Purves for Mentoring and Recursion.


--| CONTACT |-----------------------------------------------

GitHub https://github.com/johnrpenner/peaBrain
Storms Nest https://johnrolandpenner.com/index-chess.html
Facebook https://www.facebook.com/chesschessmeister

