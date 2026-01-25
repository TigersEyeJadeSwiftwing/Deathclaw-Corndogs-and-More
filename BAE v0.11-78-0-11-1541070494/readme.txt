B.A.E. - Bethesda Archive Extractor v0.11

B.A.E. can extract BA2 and BSA files.

Version History
---------------
0.01 - Initial Commit
0.02 - Significantly faster open times on all BA2s, especially Fallout4 - MeshesExtra.ba2
	which took several minutes (now takes ~1s).
0.03 - Width/Height were actually listed as Height/Width in the BA2 so non-square textures were
    incorrectly extracted.
     - Gave window a minimum width/height as Windows 10 users complained of the window being too small.
     - Can open multiple archives via the file dialog, or by dragging to the executable.
0.04 - Cube maps were being extracted incorrectly.
0.05 - Skyrim SE BSA support
0.06 - Added drag and drop to main window
     - Added application icon
	 - Added About window 
0.07 - Corrected the size sent to LZ4 for decompression, which affected only a very small number of files.
	  Please see the sticky on the Nexus page for information.
	 - Added a file filter which lets you drop a text file with a list of full or partial filenames (using wildcards).
	  This was added mostly to simplify re-extracting the files affected by the bug above. 
0.08 - 3-4x faster extraction
	 - Added a filter to the UI. Searches either filename or entire path, supports wildcards (*)
0.09 - Drag and Drop file extraction.  You can drag one or multiple files from the archive to any location 
	   on your computer, including to programs that can open the filetypes you are dragging.
	   Ctrl- or Shift- click rows to drag multiple files. The checkboxes do not matter and are used for normal Extraction.
	   NOTE: Dragging folders currently not supported.
0.10 - Fixed Select All/None which I inadvertently broke last release. Also improved the implementation to be faster.
     - Fixed read/write of extended ASCII filepaths. Only 3 vanilla FO4 filenames were affected to my knowledge (María_F.fuz, María_M.fuz, Sánchez_F.fuz)
0.11 - Added support for sRGB variants of BCn textures which were not used in official files until Creation Club and FO76. Non-sRGB BC1/2/3/7 were already fully supported.
     - Added support for BC4 textures (grayscale).
     - Added support for R8G8B8A8 and R8G8B8A8 sRGB textures. FO4 previously only used B8G8R8A8.
     - Added support for BC5 SNORM (signed normals) textures. FO4 previously only used UNORM (unsigned).
     - Added error log to the progress window which will list any files that were unsuccessfully extracted.

Credits
-------
Special thanks to ianpatt and behippo for helping with my understanding of the new BA2 formats.