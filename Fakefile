buildDir=build/
javaVersion=1.5
all <- FFMPEG_IO.jar

# TODO: generate Fakefiles on the fly in generate.bsh
FFMPEG_IO.jar <- plugin.jar/ jna-wrapper.jar/ \
	linux64/libffmpeg.so[ffmpeg/libffmpeg.so]

CLASSPATH(plugin.jar)=jna-wrapper.jar
plugin.jar <- plugin/**/* 

EXCLUDE(jna-wrapper.jar)=classes/.gitignore
jna-wrapper.jar <- classes/**/*

generate-classes[generate.bsh] <- generator.jar

generator.jar <- GenerateFFMPEGClasses.java
