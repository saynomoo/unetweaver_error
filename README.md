# unetweaver_error
Unity Project that contains compilable code, but 5.2 produces an UNetWeaver error

UNetWeaver error: Exception :System.ArgumentException: Offset and length were out of bounds for the array or count is greater than the number of elements from index to the end of the source collection.
  at System.Buffer.BlockCopy (System.Array src, Int32 srcOffset, System.Array dst, Int32 dstOffset, Int32 count) [0x000a7] in /Users/builduser/buildslave/mono-runtime-and-classlibs/build/mcs/class/corlib/System/Buffer.cs:112 
  at Mono.Cecil.Metadata.BlobHeap.Read (UInt32 index) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataReader.ReadBlob () [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataReader.InitializeAssemblyReferences () [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataReader.ReadAssemblyReferences () [0x00000] in <filename unknown>:0 
  at Mono.Cecil.ModuleDefinition.<get_AssemblyReferences>b__0 (Mono.Cecil.ModuleDefinition _, Mono.Cecil.MetadataReader reader) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.ModuleDefinition.Read[ModuleDefinition,Collection`1] (Mono.Collections.Generic.Collection`1& variable, Mono.Cecil.ModuleDefinition item, System.Func`3 read) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.ModuleDefinition.get_AssemblyReferences () [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataImporter.TryGetAssemblyNameReference (Mono.Cecil.AssemblyNameReference name_reference, Mono.Cecil.AssemblyNameReference& assembly_reference) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataImporter.ImportAssemblyName (Mono.Cecil.AssemblyNameReference name) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataImporter.ImportScope (IMetadataScope scope) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.MetadataImporter.ImportType (Mono.Cecil.TypeReference type, ImportGenericContext context) [0x00000] in <filename unknown>:0 
  at Mono.Cecil.ModuleDefinition.Import (Mono.Cecil.TypeReference type) [0x00000] in <filename unknown>:0 
  at Unity.UNetWeaver.Weaver.ImportCorLibType (System.String fullName) [0x00045] in /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/UNetWeaver.cs:1112 
  at Unity.UNetWeaver.Weaver.SetupTargetTypes () [0x00005] in /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/UNetWeaver.cs:1119 
  at Unity.UNetWeaver.Weaver.Weave (System.String assName, IEnumerable`1 dependencies, IAssemblyResolver assemblyResolver, System.String unityEngineDLLPath, System.String unityUNetDLLPath, System.String outputDir) [0x0003e] in /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/UNetWeaver.cs:1537 
  at Unity.UNetWeaver.Weaver.WeaveAssemblies (IEnumerable`1 assemblies, IEnumerable`1 dependencies, IAssemblyResolver assemblyResolver, System.String outputDir, System.String unityEngineDLLPath, System.String unityUNetDLLPath) [0x00062] in /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/UNetWeaver.cs:1640 
UnityEngine.Debug:LogError(Object)
Unity.UNetWeaver.Log:Error(String) (at /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/Program.cs:20)
Unity.UNetWeaver.Weaver:WeaveAssemblies(IEnumerable`1, IEnumerable`1, IAssemblyResolver, String, String, String) (at /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/UNetWeaver.cs:1647)
Unity.UNetWeaver.Program:Process(String, String, String, String[], String[], IAssemblyResolver, Action`1, Action`1) (at /Users/builduser/buildslave/unity/build/Extensions/Networking/Weaver/Program.cs:34)
UnityEditor.Scripting.Serialization.Weaver:WeaveUnetFromEditor(String, String, String, String, Boolean)
