# Written by Sam Tupy and released under the MIT license same as UniversalSpeech itself

windows_sources = ["cobra.c", "disphelper.c", "dolphin.c", "encoding-conversion.c", "engines.c", "jaws.c", "misc.c", "narrator.c", "nvda.c", "processlist.c", "systemaccess.c", "windows-eyes.c", "zdsr.c", "zoomtext.c", "zoomtext-guid.c"]
sources = ["obj/windows/" + i for i in windows_sources] + ["obj/UniversalSpeech.c"]
VariantDir("obj", "src", duplicate = False)
StaticLibrary("UniversalSpeechStatic", sources, CPPDEFINES = ["RELEASE", "UNIVERSAL_SPEECH_STATIC", "UNIVERSAL_SPEECH_NO_SAPI", "UNIVERSAL_SPEECH_BUILDING"])
