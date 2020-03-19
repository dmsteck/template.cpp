##########################################################################################
#                                                                           |________|
# Copyright (c) 2017 CloudNC Ltd - All Rights Reserved                         |  |
#                                                                              |__|
#        ____                                                                .  ||
#       / __ \                                                               .`~||$$$$
#      | /  \ \         /$$$$$$  /$$                           /$$ /$$   /$$  /$$$$$$$
#      \ \ \ \ \       /$$__  $$| $$                          | $$| $$$ | $$ /$$__  $$
#    / / /  \ \ \     | $$  \__/| $$  /$$$$$$  /$$   /$$  /$$$$$$$| $$$$| $$| $$  \__/
#   / / /    \ \__    | $$      | $$ /$$__  $$| $$  | $$ /$$__  $$| $$ $$ $$| $$
#  / / /      \__ \   | $$      | $$| $$  \ $$| $$  | $$| $$  | $$| $$  $$$$| $$
# | | / ________ \ \  | $$    $$| $$| $$  | $$| $$  | $$| $$  | $$| $$\  $$$| $$    $$
#  \ \_/ ________/ /  |  $$$$$$/| $$|  $$$$$$/|  $$$$$$/|  $$$$$$$| $$ \  $$|  $$$$$$/
#   \___/ ________/    \______/ |__/ \______/  \______/  \_______/|__/  \__/ \______/
#
##########################################################################################
FetchContent_Declare(
        catch_dl
        GIT_REPOSITORY https://github.com/catchorg/Catch2.git
        GIT_TAG v2.9.2
)

FetchContent_GetProperties(catch_dl)
if (NOT catch_dl_POPULATED)
    FetchContent_Populate(catch_dl)

    add_library(catch INTERFACE)
    target_include_directories(catch SYSTEM INTERFACE ${catch_dl_SOURCE_DIR}/single_include)
endif (NOT catch_dl_POPULATED)
