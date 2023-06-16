# TempDUmp
DumpForCodeError

---- Minecraft Crash Report ----
// Don't do that.

Time: 2023-06-16 20:44:01
Description: Unexpected error

java.lang.NullPointerException: Cannot invoke "net.minecraft.class_897.method_3933(net.minecraft.class_1297, net.minecraft.class_4604, double, double, double)" because "$$5" is null
	at net.minecraft.class_898.method_3950(class_898.java:131)
	at net.coderbot.iris.pipeline.ShadowRenderer.renderEntities(ShadowRenderer.java:591)
	at net.coderbot.iris.pipeline.ShadowRenderer.renderShadows(ShadowRenderer.java:483)
	at net.coderbot.iris.pipeline.newshader.NewWorldRenderingPipeline.renderShadows(NewWorldRenderingPipeline.java:1033)
	at net.minecraft.class_761.handler$bje000$iris$renderTerrainShadows(class_761.java:7037)
	at net.minecraft.class_761.method_22710(class_761.java:1241)
	at net.minecraft.class_757.method_3188(class_757.java:1110)
	at net.minecraft.class_757.method_3192(class_757.java:880)
	at net.minecraft.class_310.method_1523(class_310.java:1219)
	at net.minecraft.class_310.method_1514(class_310.java:802)
	at net.minecraft.client.main.Main.main(Main.java:250)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:468)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:74)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Render thread
Stacktrace:
	at net.minecraft.class_898.method_3950(class_898.java:131)
	at net.coderbot.iris.pipeline.ShadowRenderer.renderEntities(ShadowRenderer.java:591)
	at net.coderbot.iris.pipeline.ShadowRenderer.renderShadows(ShadowRenderer.java:483)
	at net.coderbot.iris.pipeline.newshader.NewWorldRenderingPipeline.renderShadows(NewWorldRenderingPipeline.java:1033)
	at net.minecraft.class_761.handler$bje000$iris$renderTerrainShadows(class_761.java:7037)
	at net.minecraft.class_761.method_22710(class_761.java:1241)
	at net.minecraft.class_757.method_3188(class_757.java:1110)

-- Affected level --
Details:
	All players: 1 total; [class_746['Hrbi'/33, l='ClientLevel', x=-3367.78, y=68.00, z=-2536.61]]
	Chunk stats: 1024, 0
	Level dimension: minecraft:overworld
	Level spawn location: World: (-112,72,-272), Section: (at 0,8,0 in -7,4,-17; chunk contains blocks -112,-64,-272 to -97,319,-257), Region: (-1,-1; contains chunks -32,-32 to -1,-1, blocks -512,-64,-512 to -1,319,-1)
	Level time: 79935 game time, 129369 day time
	Server brand: fabric
	Server type: Integrated singleplayer server
Stacktrace:
	at net.minecraft.class_638.method_8538(class_638.java:458)
	at net.minecraft.class_310.method_1587(class_310.java:2406)
	at net.minecraft.class_310.method_1514(class_310.java:826)
	at net.minecraft.client.main.Main.main(Main.java:250)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:468)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:74)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)

-- Last reload --
Details:
	Reload number: 1
	Reload reason: initial
	Finished: No
	Packs: vanilla, fabric, moreberries:modifiedsweetberrybushmodel
	Recovery: Yes
	Recovery reason: java.util.concurrent.CompletionException: java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_970 failed
	at java.base/java.util.concurrent.CompletableFuture.encodeThrowable(CompletableFuture.java:315)
	at java.base/java.util.concurrent.CompletableFuture.completeThrowable(CompletableFuture.java:320)
	at java.base/java.util.concurrent.CompletableFuture$UniRun.tryFire(CompletableFuture.java:791)
	at java.base/java.util.concurrent.CompletableFuture$Completion.run(CompletableFuture.java:482)
	at net.minecraft.class_4014.method_18365(class_4014.java:69)
	at net.minecraft.class_1255.method_18859(class_1255.java:156)
	at net.minecraft.class_4093.method_18859(class_4093.java:23)
	at net.minecraft.class_1255.method_16075(class_1255.java:130)
	at net.minecraft.class_1255.method_5383(class_1255.java:115)
	at net.minecraft.class_310.method_1523(class_310.java:1175)
	at net.minecraft.class_310.method_1514(class_310.java:802)
	at net.minecraft.client.main.Main.main(Main.java:250)
	at net.fabricmc.loader.impl.game.minecraft.MinecraftGameProvider.launch(MinecraftGameProvider.java:468)
	at net.fabricmc.loader.impl.launch.knot.Knot.launch(Knot.java:74)
	at net.fabricmc.loader.impl.launch.knot.KnotClient.main(KnotClient.java:23)
Caused by: java.lang.BootstrapMethodError: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_970 failed
	at net.minecraft.class_5619.<clinit>(class_5619.java:31)
	at net.minecraft.class_898.method_14491(class_898.java:397)
	at net.minecraft.class_4013.method_29490(class_4013.java:15)
	at java.base/java.util.concurrent.CompletableFuture$UniRun.tryFire(CompletableFuture.java:787)
	... 12 more
Caused by: java.lang.RuntimeException: Mixin transformation of net.minecraft.class_970 failed
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:427)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.tryLoadClass(KnotClassDelegate.java:323)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.loadClass(KnotClassDelegate.java:218)
	at net.fabricmc.loader.impl.launch.knot.KnotClassLoader.loadClass(KnotClassLoader.java:112)
	at java.base/java.lang.ClassLoader.loadClass(ClassLoader.java:520)
	... 16 more
Caused by: org.spongepowered.asm.mixin.transformer.throwables.MixinTransformerError: An unexpected critical error was encountered
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:392)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClass(MixinTransformer.java:234)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClassBytes(MixinTransformer.java:202)
	at net.fabricmc.loader.impl.launch.knot.KnotClassDelegate.getPostMixinClassByteArray(KnotClassDelegate.java:422)
	... 20 more
Caused by: org.spongepowered.asm.mixin.injection.throwables.InjectionError: Critical injection failure: Argument modifier method injectArmor(Lnet/minecraft/class_572;)Lnet/minecraft/class_572; in geckolib.mixins.json:MixinHumanoidArmorLayer from mod geckolib failed injection check, (0/1) succeeded. Scanned 1 target(s). Using refmap geckolib-fabric-1.19.4-refmap.json
	at org.spongepowered.asm.mixin.injection.struct.InjectionInfo.postInject(InjectionInfo.java:468)
	at org.spongepowered.asm.mixin.transformer.MixinTargetContext.applyInjections(MixinTargetContext.java:1384)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyInjections(MixinApplicatorStandard.java:1062)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyMixin(MixinApplicatorStandard.java:402)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.apply(MixinApplicatorStandard.java:327)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.apply(TargetClassContext.java:421)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.applyMixins(TargetClassContext.java:403)
	at org.spongepowered.asm.mixin.transformer.MixinProcessor.applyMixins(MixinProcessor.java:363)
	... 23 more


-- System Details --
Details:
	Minecraft Version: 1.20.1
	Minecraft Version ID: 1.20.1
	Operating System: Windows 10 (amd64) version 10.0
	Java Version: 17.0.3, Microsoft
	Java VM Version: OpenJDK 64-Bit Server VM (mixed mode), Microsoft
	Memory: 1406575952 bytes (1341 MiB) / 4026531840 bytes (3840 MiB) up to 6442450944 bytes (6144 MiB)
	CPUs: 4
	Processor Vendor: GenuineIntel
	Processor Name: Intel(R) Core(TM) i5-7300HQ CPU @ 2.50GHz
	Identifier: Intel64 Family 6 Model 158 Stepping 9
	Microarchitecture: Kaby Lake
	Frequency (GHz): 2.50
	Number of physical packages: 1
	Number of physical CPUs: 4
	Number of logical CPUs: 4
	Graphics card #0 name: Intel(R) HD Graphics 630
	Graphics card #0 vendor: Intel Corporation (0x8086)
	Graphics card #0 VRAM (MB): 1024.00
	Graphics card #0 deviceId: 0x591b
	Graphics card #0 versionInfo: DriverVersion=31.0.101.2111
	Graphics card #1 name: NVIDIA GeForce GTX 1060 with Max-Q Design
	Graphics card #1 vendor: NVIDIA (0x10de)
	Graphics card #1 VRAM (MB): 4095.00
	Graphics card #1 deviceId: 0x1c20
	Graphics card #1 versionInfo: DriverVersion=31.0.15.3179
	Memory slot #0 capacity (MB): 8192.00
	Memory slot #0 clockSpeed (GHz): 2.40
	Memory slot #0 type: DDR4
	Virtual memory max (MB): 20084.07
	Virtual memory used (MB): 17947.66
	Swap memory total (MB): 12000.00
	Swap memory used (MB): 2019.74
	JVM Flags: 9 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xss1M -Xmx6G -XX:+UnlockExperimentalVMOptions -XX:+UseG1GC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=50 -XX:G1HeapRegionSize=32M
	Fabric Mods: 
		absentia: Absentia 1.9
		additionallanterns: Additional Lanterns 1.0.5
		alloy_forgery: Alloy Forgery 2.0.21+1.20
		appleskin: AppleSkin 2.5.0+mc1.20
		architectury: Architectury 9.0.8
		balm-fabric: Balm 7.0.3
		bee_info: More Bee info  1.1.1
		better_climbing: Better Climbing 3
		betterarcheology: Better Archeology 1.0.1
		betterspawnercontrol: Better Spawner Control 4.2
		blockus: Blockus 2.7.1+1.20
			terraform-wood-api-v1: Terraform Wood API (v1) 7.0.0-alpha.4
		book_ofexperience_mr: Book of Experience 1-v3.0.0
		bushierflowers: Bushier Flowers 0.0.3-1.20.1
		caffeinated: Caffeinated 1.0.2
		cardinal-components: Cardinal Components API 5.2.1
			cardinal-components-base: Cardinal Components API (base) 5.2.1
			cardinal-components-block: Cardinal Components API (blocks) 5.2.1
			cardinal-components-chunk: Cardinal Components API (chunks) 5.2.1
			cardinal-components-entity: Cardinal Components API (entities) 5.2.1
			cardinal-components-item: Cardinal Components API (items) 5.2.1
			cardinal-components-level: Cardinal Components API (world saves) 5.2.1
			cardinal-components-scoreboard: Cardinal Components API (scoreboard) 5.2.1
			cardinal-components-world: Cardinal Components API (worlds) 5.2.1
		chalk: Chalk 2.2.0
			simplefabric: SimpleFabric 1.0.0
		cloth-config: Cloth Config v11 11.0.99
			cloth-basic-math: cloth-basic-math 0.6.1
		clutter: Clutter 1.20-0.3.6
		collective: Collective 6.57
		comforts: Comforts 6.3.0+1.20.1
			spectrelib: SpectreLib 0.13.11+1.20.1
				com_electronwill_night-config_core: core 3.6.5
				com_electronwill_night-config_toml: toml 3.6.5
		compose: Compose 1.3.1
		continuity: Continuity 3.0.0-beta.2+1.20
		cookingforblockheads: Cooking for Blockheads 16.0.0
		cozy: Cozy 1.1.0
			resourcefullib: Resourceful Lib 2.0.6
				com_teamresourceful_yabn: yabn 1.0.3
		cyclepaintings: Cycle Paintings 3.2
		elytratrims: Elytra Trims 1.1.5
			com_github_llamalad7_mixinextras: MixinExtras 0.2.0-beta.6
		extendedcopper: Extended Copper 1.4.1
		fabric-api: Fabric API 0.83.1+1.20.1
			fabric-api-base: Fabric API Base 0.4.29+b04edc7a77
			fabric-api-lookup-api-v1: Fabric API Lookup API (v1) 1.6.34+4d8536c977
			fabric-biome-api-v1: Fabric Biome API (v1) 13.0.10+b3afc78b77
			fabric-block-api-v1: Fabric Block API (v1) 1.0.9+e022e5d177
			fabric-blockrenderlayer-v1: Fabric BlockRenderLayer Registration (v1) 1.1.39+b3afc78b77
			fabric-client-tags-api-v1: Fabric Client Tags 1.0.20+b3afc78b77
			fabric-command-api-v1: Fabric Command API (v1) 1.2.32+f71b366f77
			fabric-command-api-v2: Fabric Command API (v2) 2.2.11+b3afc78b77
			fabric-commands-v0: Fabric Commands (v0) 0.2.49+df3654b377
			fabric-containers-v0: Fabric Containers (v0) 0.1.61+df3654b377
			fabric-content-registries-v0: Fabric Content Registries (v0) 4.0.7+b3afc78b77
			fabric-convention-tags-v1: Fabric Convention Tags 1.5.3+b3afc78b77
			fabric-crash-report-info-v1: Fabric Crash Report Info (v1) 0.2.18+aeb40ebe77
			fabric-data-generation-api-v1: Fabric Data Generation API (v1) 12.1.11+b3afc78b77
			fabric-dimensions-v1: Fabric Dimensions API (v1) 2.1.51+b3afc78b77
			fabric-entity-events-v1: Fabric Entity Events (v1) 1.5.21+b3afc78b77
			fabric-events-interaction-v0: Fabric Events Interaction (v0) 0.6.0+b3afc78b77
			fabric-events-lifecycle-v0: Fabric Events Lifecycle (v0) 0.2.61+df3654b377
			fabric-game-rule-api-v1: Fabric Game Rule API (v1) 1.0.38+b04edc7a77
			fabric-item-api-v1: Fabric Item API (v1) 2.1.26+b3afc78b77
			fabric-item-group-api-v1: Fabric Item Group API (v1) 4.0.7+b3afc78b77
			fabric-key-binding-api-v1: Fabric Key Binding API (v1) 1.0.36+fb8d95da77
			fabric-keybindings-v0: Fabric Key Bindings (v0) 0.2.34+df3654b377
			fabric-lifecycle-events-v1: Fabric Lifecycle Events (v1) 2.2.20+b3afc78b77
			fabric-loot-api-v2: Fabric Loot API (v2) 1.1.37+b3afc78b77
			fabric-loot-tables-v1: Fabric Loot Tables (v1) 1.1.41+9e7660c677
			fabric-message-api-v1: Fabric Message API (v1) 5.1.6+b3afc78b77
			fabric-mining-level-api-v1: Fabric Mining Level API (v1) 2.1.47+b3afc78b77
			fabric-models-v0: Fabric Models (v0) 0.3.35+b3afc78b77
			fabric-networking-api-v1: Fabric Networking API (v1) 1.3.8+b3afc78b77
			fabric-networking-v0: Fabric Networking (v0) 0.3.48+df3654b377
			fabric-object-builder-api-v1: Fabric Object Builder API (v1) 11.0.6+b3afc78b77
			fabric-particles-v1: Fabric Particles (v1) 1.0.28+b3afc78b77
			fabric-recipe-api-v1: Fabric Recipe API (v1) 1.0.18+b3afc78b77
			fabric-registry-sync-v0: Fabric Registry Sync (v0) 2.2.6+b3afc78b77
			fabric-renderer-api-v1: Fabric Renderer API (v1) 3.0.1+b3afc78b77
			fabric-renderer-indigo: Fabric Renderer - Indigo 1.3.1+b3afc78b77
			fabric-renderer-registries-v1: Fabric Renderer Registries (v1) 3.2.44+df3654b377
			fabric-rendering-data-attachment-v1: Fabric Rendering Data Attachment (v1) 0.3.33+b3afc78b77
			fabric-rendering-fluids-v1: Fabric Rendering Fluids (v1) 3.0.26+b3afc78b77
			fabric-rendering-v0: Fabric Rendering (v0) 1.1.47+df3654b377
			fabric-rendering-v1: Fabric Rendering (v1) 3.0.6+b3afc78b77
			fabric-resource-conditions-api-v1: Fabric Resource Conditions API (v1) 2.3.5+ea08f9d877
			fabric-resource-loader-v0: Fabric Resource Loader (v0) 0.11.7+f7923f6d77
			fabric-screen-api-v1: Fabric Screen API (v1) 2.0.6+b3afc78b77
			fabric-screen-handler-api-v1: Fabric Screen Handler API (v1) 1.3.27+b3afc78b77
			fabric-sound-api-v1: Fabric Sound API (v1) 1.0.12+b3afc78b77
			fabric-transfer-api-v1: Fabric Transfer API (v1) 3.2.2+b3afc78b77
			fabric-transitive-access-wideners-v1: Fabric Transitive Access Wideners (v1) 4.2.0+b3afc78b77
		fabricloader: Fabric Loader 0.14.21
		fallingleaves: Falling Leaves 1.15.1+1.20.1
		fallingtree: FallingTree 4.1.1
		farmingforblockheads: Farming for Blockheads 14.0.0
		floralench: Floral Enchantment Fabric-1.20.1-1.1.3
		geckolib: Geckolib 4.2
			com_eliotlash_mclib_mclib: mclib 20
		glow_ink_plus: Glow Ink Plus Mod 1.2.0
		icepreventscropgrowth: Ice Prevents Crop Growth 3.0
		indium: Indium 1.0.18+mc1.20
		integrated-circuit: Integrated Circuit 1.20-1.3.0
		iris: Iris 1.6.4
			io_github_douira_glsl-transformer: glsl-transformer 2.0.0-pre13
			org_anarres_jcpp: jcpp 1.4.14
			org_antlr_antlr4-runtime: antlr4-runtime 4.11.1
		java: OpenJDK 64-Bit Server VM 17
		journeymap: Journeymap 5.9.9
			journeymap-api-fabric: JourneyMap API 1.20-1.9-fabric-SNAPSHOT
		linkart: Linkart 5.1.1-1.19.3
		midnightlib: MidnightLib 1.4.1
		minecraft: Minecraft 1.20.1
		modmenu: Mod Menu 7.0.1
		morebannerfeatures: More Banner Features 1.2.0
		moreberries: More Berries 1.5.5
		nutritious-feast: Nutritious Feast 1.6.1
		owo: oωo 0.11.0+1.20
			blue_endless_jankson: jankson 1.2.2
		primalstorage: PrimalStorage 1.3
		rocks: This Rocks! 1.7.1
		roughlyenoughitems: Roughly Enough Items 12.0.625
			error_notifier: Error Notifier 1.0.9
		seasons: Fabric Seasons 2.2.1+1.20
		skinlayers: 3d Skin Layers 1.5.3-mc1.20
		sodium: Sodium 0.4.10+build.27
		spyglass_astronomy: Spyglass Astronomy 1.0.5-mc1.20+
		supermartijn642corelib: SuperMartijn642's Core Lib 1.1.9-b
		toggleableitemframes: Toggleable Item Frames 2.1.2-1.20.x
		trimmable_tools: Trimmable Tools 1.0.4
		trinkets: Trinkets 3.7.0
		waystones: Waystones 14.0.0
		windchimes: Windchimes 1.2.3+1.20
		yet_another_config_lib_v3: YetAnotherConfigLib 3.0.1+1.20
			com_twelvemonkeys_common_common-image: common-image 3.9.4
			com_twelvemonkeys_common_common-io: common-io 3.9.4
			com_twelvemonkeys_common_common-lang: common-lang 3.9.4
			com_twelvemonkeys_imageio_imageio-core: imageio-core 3.9.4
			com_twelvemonkeys_imageio_imageio-metadata: imageio-metadata 3.9.4
			com_twelvemonkeys_imageio_imageio-webp: imageio-webp 3.9.4
	Loaded Shaderpack: ComplementaryShaders_v4.7.2.zip
		Profile: HIGH (+0 options changed by user)
	NEC status: No NEC detected
	Launched Version: fabric-loader-0.14.21-1.20.1
	Backend library: LWJGL version 3.3.1 SNAPSHOT
	Backend API: NVIDIA GeForce GTX 1060 with Max-Q Design/PCIe/SSE2 GL version 3.2.0 NVIDIA 531.79, NVIDIA Corporation
	Window size: 1920x1080
	GL Caps: Using framebuffer using OpenGL 3.2
	GL debug messages: 
	Using VBOs: Yes
	Is Modded: Definitely; Client brand changed to 'fabric'; Server brand changed to 'fabric'
	Type: Integrated Server (map_client.txt)
	Graphics mode: fancy
	Resource Packs: 
	Current Language: en_us
	CPU: 4x Intel(R) Core(TM) i5-7300HQ CPU @ 2.50GHz
	Server Running: true
	Player Count: 1 / 8; [class_3222['Hrbi'/33, l='ServerLevel[Survival]', x=-3367.78, y=68.00, z=-2536.61]]
	Data Packs: vanilla, bundle, fabric
	Enabled Feature Flags: minecraft:bundle, minecraft:vanilla
	World Generation: Stable
