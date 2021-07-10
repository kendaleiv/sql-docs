---
title: Download and install Azure Data Studio
description: Download and install Azure Data Studio for Windows, macOS, or Linux. This article provides release dates, version numbers, system requirements, and download links.
ms.prod: azure-data-studio
ms.technology: azure-data-studio
ms.topic: overview
author: yualan
ms.author: alayu
ms.reviewer: maghan
ms.custom: seodec18, contperf-fy21q4
ms.date: 06/17/2021
---

# Download and install Azure Data Studio

Azure Data Studio is a cross-platform database tool for data professionals who use on-premises and cloud data platforms on Windows, macOS, and Linux.

Azure Data Studio offers a modern editor experience with IntelliSense, code snippets, source control integration, and an integrated terminal. It's engineered with the data platform user in mind, with the built-in charting of query result sets and customizable dashboards.

Use Azure Data Studio to query, design, and manage your databases and data warehouses wherever they are, on your local computer or in the cloud.

For more information about Azure Data Studio, visit [What is Azure Data Studio?](what-is-azure-data-studio.md).

## Download Azure Data Studio

Azure Data Studio 1.30.0 is the latest general availability (GA) version. If you have an earlier GA version installed, installing Azure Data Studio 1.28.0 updates it to the latest version.

- Release number: 1.30.0
- Release date: June 17, 2021

| Platform | Download |
|----------|----------|
| Windows | [User installer](https://go.microsoft.com/fwlink/?linkid=2165736) (recommended)<br>[System installer](https://go.microsoft.com/fwlink/?linkid=2165737)<br>[.zip file](https://go.microsoft.com/fwlink/?linkid=2165838) |
| macOS | [.zip file](https://go.microsoft.com/fwlink/?linkid=2165942) |
| Linux | [.deb file](https://go.microsoft.com/fwlink/?linkid=2165738)<br>[.rpm file](https://go.microsoft.com/fwlink/?linkid=2165842)<br>[.tar.gz file](https://go.microsoft.com/fwlink/?linkid=2165841) |
| | |

> [!Note]
> Azure Data Studio currently does not support the ARM architecture.

If you have comments or suggestions or want to report a problem with downloading Azure Data Studio, submit an issue to our team on the [Azure Data Studio feedback page](https://github.com/microsoft/azuredatastudio/issues/).

## Install Azure Data Studio

### Windows installation

[!INCLUDE [ssms-ads-install](../includes/ssms-azure-data-studio-install.md)]

This release of Azure Data Studio includes a standard Windows installer experience and a .zip file.

We recommend the *user installer*, which simplifies installations and updates and doesn't require Administrator privileges. (It doesn't require Administrator privileges because the location is under your user Local AppData (LOCALAPPDATA) folder.) The user installer also provides a smoother background update experience. For more information, see [User setup for Windows](https://code.visualstudio.com/updates/v1_26#_user-setup-for-windows).

**User installer** (recommended)

1. Download and run the [Azure Data Studio user installer for Windows](https://go.microsoft.com/fwlink/?linkid=2165736).

2. Start the Azure Data Studio app.

**System installer**

1. Download and run the [Azure Data Studio system installer for Windows](https://go.microsoft.com/fwlink/?linkid=2165737).

2. Start the Azure Data Studio app.

**.zip file**

1. Download the [Azure Data Studio .zip file for Windows](https://go.microsoft.com/fwlink/?linkid=2165838).

2. Go to the downloaded file and extract it.

3. Run `\azuredatastudio-windows\azuredatastudio.exe`.

#### Unattended installation for Windows

You can also install Azure Data Studio by using a command prompt script.

For Windows, install Azure Data Studio in the background without prompts by doing the following:

1. Open the command prompt window with elevated permissions.

2. Run the following command:

    ```console
    <path where the azuredatastudio-windows-user-setup-x.xx.x.exe file is located> /VERYSILENT /MERGETASKS=!runcode>
    ```

    Example:

    ```console
    %systemdrive%\azuredatastudio-windows-user-setup-1.24.0.exe /VERYSILENT /MERGETASKS=!runcode
    ```

    > [!Note]
    > The following example also works with the system installer file.
    > 
    > ```console
    > <path where the azuredatastudio-windows-setup-x.xx.x.exe file is located> /VERYSILENT /MERGETASKS=!runcode>
    > ```
    >
    > In the preceding code, you can also pass */SILENT* instead of */VERYSILENT* to see the setup user interface.

3. If you've run the commands successfully, you can see Azure Data Studio installed.

### macOS installation

1. Download [Azure Data Studio for macOS](https://go.microsoft.com/fwlink/?linkid=2165942).

2. To expand the contents of the .zip file, double-click it.

3. To make Azure Data Studio available in Launchpad, drag the *Azure Data Studio.app* file to the *Applications* folder.

### Linux installation

#### Install with a .deb file

1. Download Azure Data Studio for Linux by using the [.deb](https://go.microsoft.com/fwlink/?linkid=2165738) file.

2. To extract the .deb file, open a new terminal window, and then run the following commands:

    ```bash
    cd ~
    sudo dpkg -i ./Downloads/azuredatastudio-linux-<version string>.deb
    ```

3. To start Azure Data Studio, run this command:

    ```bash
    azuredatastudio
    ```

> [!Note]
> You might have missing dependencies. To install them, run the following command:
>
> ```bash
> sudo apt-get install libunwind8
> ```

#### Install with an .rpm file

1. Download Azure Data Studio for Linux by using the [.rpm](https://go.microsoft.com/fwlink/?linkid=2165842) file.

2. To extract the file, open a new terminal window, and then run the following commands:

    ```bash
    cd ~
    yum install ./Downloads/azuredatastudio-linux-<version string>.rpm
    ```

3. To start Azure Data Studio, run this command:

    ```bash
    azuredatastudio
    ```

> [!Note]
> You might have missing dependencies. To install them, run the following command:
>
> ```bash
> yum install libXScrnSaver
> ```

#### Install with a .tar.gz file

1. Download Azure Data Studio for Linux by using the [.tar.gz](https://go.microsoft.com/fwlink/?linkid=2165841) file.

2. To extract the file, open a new terminal window, and then run the following commands:

    ```bash
    cd ~
    cp ~/Downloads/azuredatastudio-linux-<version string>.tar.gz ~ 
    tar -xvf ~/azuredatastudio-linux-<version string>.tar.gz 
    echo 'export PATH="$PATH:~/azuredatastudio-linux-x64"' >> ~/.bashrc
    source ~/.bashrc
    ```

3. To start Azure Data Studio, run this command:

    ```bash
    azuredatastudio
    ```
    
> [!Note] 
> You might have missing dependencies. To install them, run the following command:
>
> ```bash
> sudo apt-get install libxss1 libgconf-2-4 libunwind8
> ```



#### Windows Subsystem for Linux

1. Install Azure Data Studio for Windows. Then, use the `azuredatastudio` command in a Windows Subsystem for Linux (WSL) terminal just as you would in a standard command prompt. By default, the application is stored in your *AppData* folder.

2. Start Azure Data Studio from the WSL command prompt. When you're using the default Windows installation, start the application by running the following command:

    ```bash
    '/mnt/c/Users/<your user name>/AppData/Local/Programs/Azure Data Studio/azuredatastudio.exe'
    ```

## What's new with Azure Data Studio

For details about the latest release of Azure Data Studio, see [Release notes for Azure Data Studio](./release-notes-azure-data-studio.md).

## Download the GA release of Azure Data Studio
    
We recommend that you [download the general availability (GA) release of Azure Data Studio](#download-azure-data-studio). 
    
## Download the insiders build of Azure Data Studio    

As an alternative, if you want to try out the beta features and send feedback, you can [download the insiders build of Azure Data Studio](https://github.com/microsoft/azuredatastudio#try-out-the-latest-insiders-build-from-main).

## Supported operating systems

Azure Data Studio runs on Windows, macOS, and Linux and is supported on the following platforms:

### Windows operating systems

- Windows 10 (64-bit)
- Windows 8.1 (64-bit)
- Windows 8 (64-bit)
- Windows 7 (SP1)
- Windows Server 2019
- Windows Server 2016
- Windows Server 2012 R2 (64-bit)
- Windows Server 2012 (64-bit)
- Windows Server 2008 R2 (64-bit)

### macOS operating systems

- macOS 10.15 Catalina
- macOS 10.14 Mojave
- macOS 10.13 High Sierra
- macOS 10.12 Sierra
- macOS 11.1  Big Sur

### Linux operating systems

- Red Hat Enterprise Linux (RHEL) 8.3
- Red Hat Enterprise Linux 8.2
- Red Hat Enterprise Linux 8.1
- Red Hat Enterprise Linux 8.0
- Red Hat Enterprise Linux 7.4
- Red Hat Enterprise Linux 7.3
- SUSE Linux Enterprise Server v12 SP2
- Ubuntu 20.04
- Ubuntu 18.04
- Ubuntu 16.04

> [!Note]
>
> Versions 7.3 and 7.4 of RHEL are no longer supported by Red Hat. RHEL 7.3 support ended November 30, 2018, and RHEL 7.4 ended August 31, 2019.
>
> For more information, see the [RHEL 7 Application Compatibility Guide](https://access.redhat.com/articles/rhel-abi-compatibility) or the [RHEL 8 Application Compatibility Guide](https://access.redhat.com/articles/rhel8-abi-compatibility).

## System requirements

| Requirement level | CPU cores | RAM memory |
| --- | :---: | :---: |
| Recommended | 4 | 8 GB |
| Minimum | 2 | 4 GB |

## Check for updates

To check for the latest updates, on the left pane, select **Manage** (gear icon), and then select **Check for Updates**.

To apply environment updates offline, [install the latest version](#download-and-install-azure-data-studio) directly over your previously installed version. You don't need to uninstall earlier versions of Azure Data Studio. If an earlier version is present, the installer automatically updates to the latest version.

## Move user settings

If you're updating SQL Operations Studio to Azure Data Studio and want to keep your settings, keyboard shortcuts, or code snippets, do the following:

> [!NOTE]
> If you've already installed Azure Data Studio or you've never installed or customized SQL Operations Studio, you can ignore this section.

1. On the left pane, select **Manage** (gear icon) and then select **Settings.**

   ![Screenshot of the Azure Data Studio "Manage" icon and "Settings" command.](./media/download/open-settings.png)

1. At the top, right-click the **User Settings** tab, and then select **Reveal in Explorer**.

   ![Screenshot of the "Reveal in Explorer" command in the "User Settings" tab.](./media/download/reveal-in-explorer.png)

1. Copy all files in this folder and save them in an easy-to-find location on your local drive, such as your *Documents* folder.

   ![Screenshot of the settings.json file in the Windows Explorer folder structure.](./media/download/copy-settings.png)

1. In your updated version of Azure Data Studio, follow steps 1 and 2 and then, for step 3, paste the contents you saved into the folder. You can also manually copy over the settings, key bindings, or snippets in their respective locations.

1. If you're overriding your current installation, before you do so, delete the old installation directory to avoid errors connecting to your Azure account for the resource explorer.

## Uninstall Azure Data Studio from Windows

If you installed Azure Data Studio by using the Windows installer, uninstall it just as you would any Windows application.

If you installed Azure Data Studio with a .zip file or other archive, delete that file.

## Uninstall Azure Data Studio from macOS

You can [uninstall apps](https://support.apple.com/guide/mac-help/install-and-uninstall-other-apps-mh35835/mac) from the internet or disc on Mac by doing the following:

1. Select the **Finder icon** in the Dock, and then select **Applications** in the **Finder** sidebar.

2. Do one of the following:

    - If an app is in a folder, open the app's folder to check for an uninstaller. Double-click **Uninstall [App]** or **[App] Uninstaller**, and then follow the onscreen instructions.

    - If an app isn't in a folder or doesn't have an uninstaller, drag the app from the *Applications* folder to the Trash (at the end of the Dock).

To uninstall apps you've downloaded from the App Store, use Launchpad.

## Uninstall Azure Data Studio from Linux

### In Debian

You can uninstall Azure Data Studio under Debian or Ubuntu Linux.

To list installed software type, run the following commands:

```bash
dpkg --list
dpkg --list | less
dpkg --list | grep apache
```

To delete the software, run the following commands:

```bash
sudo apt-get remove azuredatastudio
sudo apt-get remove apache
```

### In RedHat

Use the rpm or yum command to delete Azure Data Studio.

To list the installed software type, run the following commands:

```bash
rpm -qa | less
rpm -qa azuredatastudio
yum list | less
yum list azuredatastudio
```

To get information about the azuredatastudio package, run the following commands:

```bash
rpm -qa azuredatastudio
yum list azuredatastudio
```

To delete a package called azuredatastudio, run the following commands:

```bash
rpm -e azuredatastudio
yum remove azuredatastudio
```

## Next steps

To learn more about Azure Data Studio, see the following resources:

- [Azure Data Studio release notes](release-notes-azure-data-studio.md)
- [What is Azure Data Studio?](what-is-azure-data-studio.md)
- [SQL tools](../tools/overview-sql-tools.md)
- [Azure Data Architecture Guide](/azure/architecture/data-guide/)
- [SQL Server Blog](https://cloudblogs.microsoft.com/sqlserver/)

[!INCLUDE[get-help-sql-tools](../includes/paragraph-content/get-help-sql-tools.md)]

[!INCLUDE[contribute-to-content](../includes/paragraph-content/contribute-to-content.md)]

[Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839) and [Enable or disable usage data collection for Azure Data Studio](usage-data-collection.md).
