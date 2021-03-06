
cmake_minimum_required (VERSION 2.6)
project (MCServer)

include_directories ("${PROJECT_SOURCE_DIR}/../")

SET (SRCS
	BioGen.cpp
	Caves.cpp
	ChunkDesc.cpp
	ChunkGenerator.cpp
	CompoGen.cpp
	CompoGenBiomal.cpp
	ComposableGenerator.cpp
	DistortedHeightmap.cpp
	DungeonRoomsFinisher.cpp
	EndGen.cpp
	FinishGen.cpp
	GridStructGen.cpp
	HeiGen.cpp
	MineShafts.cpp
	NetherFortGen.cpp
	Noise3DGenerator.cpp
	POCPieceGenerator.cpp
	PieceGenerator.cpp
	Prefab.cpp
	PrefabPiecePool.cpp
	RainbowRoadsGen.cpp
	Ravines.cpp
	RoughRavines.cpp
	StructGen.cpp
	TestRailsGen.cpp
	Trees.cpp
	TwoHeights.cpp
	UnderwaterBaseGen.cpp
	VillageGen.cpp
)

SET (HDRS
	BioGen.h
	Caves.h
	ChunkDesc.h
	ChunkGenerator.h
	CompoGen.h
	CompoGenBiomal.h
	ComposableGenerator.h
	CompositedHeiGen.h
	DistortedHeightmap.h
	DungeonRoomsFinisher.h
	EndGen.h
	FinishGen.h
	GridStructGen.h
	HeiGen.h
	IntGen.h
	MineShafts.h
	NetherFortGen.h
	Noise3DGenerator.h
	POCPieceGenerator.h
	PieceGenerator.h
	Prefab.h
	PrefabPiecePool.h
	ProtIntGen.h
	RainbowRoadsGen.h
	Ravines.h
	RoughRavines.h
	ShapeGen.cpp
	StructGen.h
	TestRailsGen.h
	Trees.h
	TwoHeights.h
	UnderwaterBaseGen.h
	VillageGen.h
)

if(NOT MSVC)
	add_library(Generating ${SRCS} ${HDRS})

	target_link_libraries(Generating OSSupport Blocks)
endif()
