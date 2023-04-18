TagLib.Audio
=====================

**IMPORTANT - PLEASE READ**
==============
Project Information
=
This is a fork of the popular TagLib.Portable project.  

> TagLib is a library for reading and editing the meta-data of several popular audio formats.
 Currently it supports both ID3v1 and ID3v2 for MP3 files, Ogg Vorbis comments and ID3 tags and Vorbis comments in FLAC, MPC, Speex, WavPack TrueAudio, WAV, AIFF, MP4 and ASF files.

Sample Usage
=
To read in an MP3 file (using WinRT as an example):

    // assume you've got to the point where you have a StorageFile 
    // via a file picker or something similar
    
    var fileStream = await (StorageFile)file.OpenStreamForReadAsync();

	var tagFile = TagLib.File.Create(new StreamFileAbstraction(file.Name,
					 fileStream, fileStream);

	var tags = tagFile.GetTag(TagTypes.Id3v2);

	Debug.WriteLine(tags.Title);

There are other ways you can do this as well and this is just a simplest example.
