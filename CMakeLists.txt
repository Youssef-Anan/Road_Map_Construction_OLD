cmake_minimum_required(VERSION 3.28)
project(Road_Map_Construction)
#(change Road_Map_Construction to your project name)


set(CMAKE_CXX_STANDARD 17)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)


set(Qt6_DIR $ENV{QT_DIR})


find_package(Qt6 COMPONENTS Core Gui Widgets Charts REQUIRED) #lw enta Qt6 khalek zy manta lw Qt5 ghyr ay Qt6 khaleha Qt5


add_executable(Road_Map_Construction "Main Classes/main.cpp"
        "Headers/FIle_Handler.h"
        "Headers/Graph.h"
        "Headers/User_Interface.h"
        "Graph Classes/Graph.cpp"
        "User Interface Classes/User_Interface.cpp"
        "GUI Classes/graphpage.h"
        "GUI Classes/welcomepage.h"
)


target_link_libraries(Road_Map_Construction PRIVATE Qt6::Core Qt6::Gui Qt6::Widgets Qt6::Charts)
#(change Road_Map_Construction to your project name)lw enta Qt6 khalek zy manta lw Qt5 ghyr ay Qt6 khaleha Qt5
add_executable(NoGUI_Executable "Main Classes/MainNoGUI.cpp"
        "Headers/FIle_Handler.h"
        "Headers/Graph.h"
        "Headers/User_Interface.h"
        "Graph Classes/Graph.cpp"
        "User Interface Classes/User_Interface.cpp"
      )

