# 7z sdk
if(WIN32)
	add_library(3rdparty_7z STATIC EXCLUDE_FROM_ALL
		src/Sha256.c
		src/Ppmd7Dec.c
		src/XzDec.c
		src/XzEnc.c
		src/Lzma2Dec.c
		src/XzCrc64.c
		src/DllSecur.c
		src/Lzma2DecMt.c
		src/BraIA64.c
		src/7zFile.c
		src/7zStream.c
		src/Lzma86Enc.c
		src/Threads.c
		src/7zAlloc.c
		src/LzmaEnc.c
		src/MtCoder.c
		src/Lzma86Dec.c
		src/Sort.c
		src/LzFindMt.c
		src/7zDec.c
		src/Bcj2.c
		src/Ppmd7.c
		src/Bra86.c
		src/Bcj2Enc.c
		src/7zBuf.c
		src/Aes.c
		src/AesOpt.c
		src/XzCrc64Opt.c
		src/7zArcIn.c
		src/Lzma2Enc.c
		src/Bra.c
		src/7zCrcOpt.c
		src/7zBuf2.c
		src/LzFind.c
		src/Ppmd7Enc.c
		src/CpuArch.c
		src/Delta.c
		src/XzIn.c
		src/Alloc.c
		src/Xz.c
		src/LzmaDec.c
		src/LzmaLib.c
		src/7zCrc.c
		src/MtDec.c)
	target_include_directories(3rdparty_7z INTERFACE
		$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/src>
		$<INSTALL_INTERFACE:/src>)

	target_include_directories(3rdparty_7z INTERFACE 7z)

	set_property(TARGET 3rdparty_7z PROPERTY FOLDER "3rdparty/")

else()
	add_library(3rdparty_7z INTERFACE)
endif()
