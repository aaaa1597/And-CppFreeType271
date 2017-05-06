cmake_minimum_required(VERSION 3.4.1)

include_directories(src/main/cpp/freetype271/inc)

add_library( freetype271 SHARED
                src/main/cpp/testmain.cpp
                src/main/cpp/freetype271/autofit/autofit.c
                src/main/cpp/freetype271/bdf/bdf.c
                src/main/cpp/freetype271/cff/cff.c
                src/main/cpp/freetype271/base/ftbase.c
                src/main/cpp/freetype271/base/ftbitmap.c
                src/main/cpp/freetype271/cache/ftcache.c
                src/main/cpp/freetype271/base/ftdebug.c
                src/main/cpp/freetype271/base/ftfstype.c
                src/main/cpp/freetype271/base/ftgasp.c
                src/main/cpp/freetype271/base/ftglyph.c
                src/main/cpp/freetype271/gzip/ftgzip.c
                src/main/cpp/freetype271/base/ftinit.c
                src/main/cpp/freetype271/lzw/ftlzw.c
                src/main/cpp/freetype271/base/ftstroke.c
                src/main/cpp/freetype271/base/ftsystem.c
                src/main/cpp/freetype271/smooth/smooth.c
                src/main/cpp/freetype271/truetype/truetype.c
                src/main/cpp/freetype271/type1/type1.c
                src/main/cpp/freetype271/cid/type1cid.c
                src/main/cpp/freetype271/pcf/pcf.c
                src/main/cpp/freetype271/pfr/pfr.c
                src/main/cpp/freetype271/psaux/psaux.c
                src/main/cpp/freetype271/type42/type42.c
                src/main/cpp/freetype271/psnames/psnames.c
                src/main/cpp/freetype271/pshinter/pshinter.c
                src/main/cpp/freetype271/raster/raster.c
                src/main/cpp/freetype271/sfnt/sfnt.c
                src/main/cpp/freetype271/winfonts/winfnt.c
                )

add_definitions(-DFT2_BUILD_LIBRARY)

find_library( log-lib log )

target_link_libraries( freetype271 ${log-lib} )
