
# CONFIG WutheringWave by KepoAmatLo
## Deskripsi

Konfigurasi untuk merubah konfigurasi grafik agar lancar untuk `hp kentang` serasa pake redmagic.

Disini ada beberapa konfigurasi grafis yang di buat untuk memaksimalkan kinerja GPU 
(Caranya ngurangin beban kerja gpu, kalo ngilangin beban ortu masih susah huhuhu T-T)

Konfigurasi ini masih dalam tahap pembuatan jadi kadang masih ada masalah dikit.
## Description 
Graphics configuration to make it smooth for mobile device. 

Here I'm make some graphics configurations that are made to maximize GPU performance (The way to reduce the GPU workload by reducing some effect)

This setting use The `Scalability settings` that allow you to adjust the quality of various features in order to maintain the best performance for your game on different platforms and hardware.

This configuration is still on development progress stage so sometimes there are still a few problems.

# How to use
To use this configuration first you need to copy `engine.ini` & `deviceprofile.ini` to
```bash
../Android/data/com.kurogame.wutheringwaves.global/files/UE4Game/Client/Client/Saved/Config/Android
```
## Cara Pasang
Cara pasangnya gampang kok, tinggal copy aja
`engine.ini` & `deviceprofile.ini` ke folder gamenya aja. Kalo gatau foldernya ada di
```bash
/data/media/0/Android/data/com.kurogame.wutheringwaves.global/files/UE4Game/Client/Client/Saved/Config/Android
```
Itu directori dari root hehehe :D jadi yang /data/media/0 itu cuma buat ke internal xD



## Contact
[![Discord](https://dcbadge.limes.pink/api/shield/1268259084906266696)](https://discord.com/users/1268259084906266696)

[![IWHYKTUSP](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)](https://Instagram.com/iwhyktusp)

[![X](https://img.shields.io/badge/X-%23000000.svg?style=for-the-badge&logo=X&logoColor=white)](https://x.com/iwhyktusp?s=09)

## How I make this configuration 
Basically Wuthering Wave is using Unreal Engine [Wuthering Wave Game information from Wiki](https://en.m.wikipedia.org/wiki/Wuthering_Waves). So I think I know how to configure some graphic settings `*.ini` files like `engine.ini` & `deviceprofile.ini` to make it run easier.
I have learning to make this graphic configuration before from some games like DS and Skyrim
And ENB (see on documentation) for some games too. 
### Here some details from ducumentation

#### View Distance
Objects can be culled based on their distance to the viewer. By default, all objects are not distance culled (Desired max draw distance of 0). On top of the designer specified value, there is a global scalability setting working like a multiplier `r.ViewDistanceScale`. Here you can see some grass objects (Desired max draw distance of 1000):
#### Anti Aliasing
Adjusting the Anti-Aliasing quality level using the `r.PostProcessAAQuality` console command will adjust the quality of whichever Anti-Aliasing method you are using (FXAA or Temporal AA). For either Anti-Aliasing method, a value of 0 used with `r.PostProcessAAQuality` will disable the effect. For FXAA, the effect of values 2, 4, and 6, can be seen in the above image; the smoothing of jagged edges becomes better and better. Values above 6 have no effect.
#### Textures - sg.TextureQuality
A modern rendering engine requires a lot more GPU memory (textures, meshes, GBuffer, Depth Buffer, Shadow maps). Some of those scale with the screen resolution (e.g. GBuffer), others with specific quality settings (e.g. Shadow maps). Another large amount comes from the used textures (usually compressed and streamed). You can instruct the streaming system to be more aggressive in management (smaller pool size, culling unused textures) or to have less or more detail in the mip level computation. This can have effects on the image quality, how much you can notice texture streaming artifacts and how smooth the game runs (updates require expensive memory transfers). The results can vary, depending on the media (e.g. faster/lower hard drive /SSD). Streaming from a DVD/Blu-Ray adds much more latency so you should try to avoid that.

The texture quality also affects the texture filtering mode `r.MaxAnisotropy`. Limiting the anisotropic sample count reduces texture bandwidth, but does not save texture memory.

For Temporal AA, there is a trade off between fill speed of the effect and quality, the higher the value you use. `r.PostProcessAAQuality 2` with Temporal AA is fast to settle but jitter caused by the effect will be more pronounced. `r.PostProcessAAQuality 4` will settle slower but will not jitter.
#### Grass and Foliage Scalability
The View -> Engine Scalability Settings -> Foliage option adjusts how many foliage meshes are rendered at one time in accordance with the settings found in the `BaseScalability.ini` file located in [UE_InstallPath]/Engine/Config folder. With the Low setting equating to `FoliageQuality 0` and Epic to `FoliageQuality 3`.

## Documentation
#### I think it will usefull

[Unreal Engine Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/scalability-reference-for-unreal-engine?application_version=5.4)

[Configuration Files | Unreal engine documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/configuration-files?application_version=4.27)

[How to store variables to a custom .ini file?](https://forums.unrealengine.com/t/how-to-store-variables-to-a-custom-ini-file/330274)

[What is ENB](https://www.reddit.com/r/skyrimmods/wiki/enb/#:~:text=ENB%20is%20a%20program%20developed,scattered%20documentation%20and%20complex%20explanations.)
