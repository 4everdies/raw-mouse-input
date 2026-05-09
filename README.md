# Raw Input

A utility mod for Minecraft 1.8.9 (Forge) that enables true raw mouse input by bypassing operating system mouse acceleration and smoothing.

This modification replaces Minecraft’s default mouse handler with a low-level raw input implementation using JInput, providing more consistent and precise aim movement.

# Requirements

* **Forge 1.8.9**
* **JDK 8** (for compiling)
* JInput native libraries

# How It Works

Normally, Minecraft receives mouse movement through the default LWJGL input system, which may still be affected by operating system acceleration and filtering.

This mod:

1. Creates a dedicated polling thread
2. Reads raw mouse delta values directly from the device
3. Injects the movement into Minecraft’s camera system

This results in more accurate and responsive camera movement, especially useful for PvP and competitive gameplay.

# How to Build (Compile)

This project strictly requires **JDK 8**.

## Windows

1. Open CMD inside the project folder.
2. Set your Java 8 path.
3. Run the Gradle build command.

```bat
set "JAVA_HOME=C:\Program Files\Java\jdk1.8.0_xxx"
gradlew clean build
```

## Linux

```bash
export JAVA_HOME=/path/to/jdk8
chmod +x gradlew
./gradlew clean build
```

The compiled `.jar` file will be generated at:
```txt
build/libs/
```

# How to Install

1. Download the latest release from the releases page.
2. Place the `.jar` file inside your Minecraft `mods` folder.
3. Launch Minecraft using **Forge 1.8.9**.
5. Enjoy native raw mouse movement.

# Disclaimer

This project was created for educational and customization purposes.
The author is not responsible for bans, punishments, hardware issues, or any other consequences resulting from the use of this modification. Use at your own risk.

Minecraft modifications are allowed under Mojang's guidelines:

[https://help.minecraft.net/hc/en-us/articles/4409139065613-Mods-for-Minecraft-Java-Edition](https://help.minecraft.net/hc/en-us/articles/4409139065613-Mods-for-Minecraft-Java-Edition)
