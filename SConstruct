# Written by Sam Tupy and released under the MIT license same as UniversalSpeech itself

runtime_libs = {"MultiThreaded": "/MT", "MultiThreadedDLL": "/MD", "MultiThreadedDebug": "/MTd", "MultiThreadedDebugDLL": "/MDd"}
runtime_lib = runtime_libs[ARGUMENTS.get("runtime", "MultiThreadedDebug" if ARGUMENTS.get("debug", "0") == "1" else "MultiThreaded")]
windows_sources = ["cobra.c", "disphelper.c", "dolphin.c", "encoding-conversion.c", "engines.c", "jaws.c", "misc.c", "narrator.c", "nvda.c", "processlist.c", "systemaccess.c", "windows-eyes.c", "zdsr.c", "zoomtext.c", "zoomtext-guid.c"]
sources = ["obj/windows/" + i for i in windows_sources] + ["obj/UniversalSpeech.c"]
debug_def = "DEBUG" if ARGUMENTS.get("debug", "0") == "1" else "NDEBUG"
VariantDir("obj", "src", duplicate = False)
StaticLibrary("UniversalSpeechStatic", sources, CPPFLAGS = [runtime_lib], CPPDEFINES = [debug_def, "UNIVERSAL_SPEECH_STATIC", "UNIVERSAL_SPEECH_NO_SAPI", "UNIVERSAL_SPEECH_BUILDING"])
