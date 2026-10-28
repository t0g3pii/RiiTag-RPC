# RiiTag-RPC

![](https://img.shields.io/github/downloads/t0g3pii/RiiTag-RPC/total)
![](https://img.shields.io/github/actions/workflow/status/t0g3pii/RiiTag-RPC/build.yml)
![](https://img.shields.io/github/commit-activity/m/t0g3pii/RiiTag-RPC)
![](https://img.shields.io/github/last-commit/t0g3pii/RiiTag-RPC)

RiiTag-RPC allows you to show your Discord friends what you're playing on your Wii or Wii U by connecting to your [RiiTag](https://riitag.t0g3pii.de/) account.

## Instructions
1. Grab the latest release from [here](https://github.com/t0g3pii/RiiTag-RPC/releases/latest) or build manually.

    Build instructions:
    - Requirements: Python 3.11

    **Windows:**
    ```powershell
    py -3.11 -m venv .venv
    .\.venv\Scripts\python.exe -m pip install -r requirements.txt pyinstaller
    .\.venv\Scripts\python.exe -m PyInstaller riitag-rpc.spec
    .\dist\riitag-rpc.exe
    ```

    **macOS and Linux:**
    ```bash
    python3.11 -m venv .venv # Alternatively using uv: uv venv --python 3.11 .venv
    .venv/bin/python -m pip install -r requirements.txt pyinstaller # Using uv: uv pip install --python .venv/bin/python -r requirements.txt pyinstaller
    .venv/bin/python -m PyInstaller riitag-rpc.spec
    ./dist/riitag-rpc
    ```
    Executable will be located in `dist/`.
2. Follow the instructions available [here](/GUIDE.md#riitag-rpc).

## Running on Raspberry Pi
It is possible to run RiiTag-RPC on your Raspberry Pi. Only the 4B model has been tested, but you may have luck on other models as well.
Please note that support for this platform is provided on a best-effort basis.

Since Discord does not have an official arm build for their client, you can use [ArmCord](https://github.com/ArmCord/ArmCord) (version **3.2.1** or higher).
We recommend installing it from [Pi-Apps](https://github.com/Botspot/pi-apps), as it makes it easy to keep the client up-to-date.

After installing ArmCord and logging in, RiiTag-RPC should work without issues.

RiiConnect24 is not affiliated with any of these projects. Please report any issues directly to their developers.

## Reporting Issues
Please report any bugs by [creating an issue](https://github.com/t0g3pii/RiiTag-RPC/issues/new).
