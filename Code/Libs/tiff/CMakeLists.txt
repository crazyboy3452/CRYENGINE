set(THIS_PROJECT tiff)

project( ${THIS_PROJECT} )

#START-FILE-LIST
# File List auto generated by waf2cmake.py, do not modify manually.

set (SourceGroup_Config
	tif_config.h
	tiffconf.h
)
source_group("Config" FILES ${SourceGroup_Config})


set (SourceGroup_Root
	../../SDKs/tiff-4.0.4/libtiff/tif_aux.c
	../../SDKs/tiff-4.0.4/libtiff/tif_close.c
	../../SDKs/tiff-4.0.4/libtiff/tif_codec.c
	../../SDKs/tiff-4.0.4/libtiff/tif_color.c
	../../SDKs/tiff-4.0.4/libtiff/tif_compress.c
	../../SDKs/tiff-4.0.4/libtiff/tif_dir.c
	../../SDKs/tiff-4.0.4/libtiff/tif_dirinfo.c
	../../SDKs/tiff-4.0.4/libtiff/tif_dirread.c
	../../SDKs/tiff-4.0.4/libtiff/tif_dirwrite.c
	../../SDKs/tiff-4.0.4/libtiff/tif_dumpmode.c
	../../SDKs/tiff-4.0.4/libtiff/tif_error.c
	../../SDKs/tiff-4.0.4/libtiff/tif_extension.c
	../../SDKs/tiff-4.0.4/libtiff/tif_fax3.c
	../../SDKs/tiff-4.0.4/libtiff/tif_fax3sm.c
	../../SDKs/tiff-4.0.4/libtiff/tif_flush.c
	../../SDKs/tiff-4.0.4/libtiff/tif_getimage.c
	../../SDKs/tiff-4.0.4/libtiff/tif_jbig.c
	../../SDKs/tiff-4.0.4/libtiff/tif_jpeg.c
	../../SDKs/tiff-4.0.4/libtiff/tif_jpeg_12.c
	../../SDKs/tiff-4.0.4/libtiff/tif_luv.c
	../../SDKs/tiff-4.0.4/libtiff/tif_lzma.c
	../../SDKs/tiff-4.0.4/libtiff/tif_lzw.c
	../../SDKs/tiff-4.0.4/libtiff/tif_next.c
	../../SDKs/tiff-4.0.4/libtiff/tif_ojpeg.c
	../../SDKs/tiff-4.0.4/libtiff/tif_open.c
	../../SDKs/tiff-4.0.4/libtiff/tif_packbits.c
	../../SDKs/tiff-4.0.4/libtiff/tif_pixarlog.c
	../../SDKs/tiff-4.0.4/libtiff/tif_predict.c
	../../SDKs/tiff-4.0.4/libtiff/tif_print.c
	../../SDKs/tiff-4.0.4/libtiff/tif_read.c
	../../SDKs/tiff-4.0.4/libtiff/tif_strip.c
	../../SDKs/tiff-4.0.4/libtiff/tif_swab.c
	../../SDKs/tiff-4.0.4/libtiff/tif_thunder.c
	../../SDKs/tiff-4.0.4/libtiff/tif_tile.c
	../../SDKs/tiff-4.0.4/libtiff/tif_unix.c
	../../SDKs/tiff-4.0.4/libtiff/tif_version.c
	../../SDKs/tiff-4.0.4/libtiff/tif_warning.c
	../../SDKs/tiff-4.0.4/libtiff/tif_write.c
	../../SDKs/tiff-4.0.4/libtiff/tif_zip.c
)


# Support unity build with uber files
set(NoUberFile ${SourceGroup_Config} ${SourceGroup_Root}  )


set (SOURCES
	${NoUberFile}
)
#END-FILE-LIST


include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )
include_directories( ${SDK_DIR}/tiff-4.0.3/libtiff )
include_directories( ${SDK_DIR}/zlib-1.2.8 )

add_library( ${THIS_PROJECT} STATIC ${SOURCES})

#USE_MSVC_PRECOMPILED_HEADER( ${THIS_PROJECT} "StdAfx.h" "StdAfx.cpp" )

SET_PLATFORM_TARGET_PROPERTIES( ${THIS_PROJECT} )