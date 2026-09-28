# Citopy Recovery Guide

### Data recovery and system recovery procedures for CitopyOS

In cases of data loss, corruption, forgotten passwords, or recovery errors, **CitopyOS may redirect you to this guide**.

> [!WARNING]
> Recovery procedures can modify system data and, depending on the method used, may result in **permanent data loss**. Follow every step exactly as described.

> [!TIP]
> For the best results, keep the device and all required storage components connected throughout the recovery process unless a specific step instructs you to disconnect or remove one.

---

## Definitions

<details>
<summary>Click to see</summary>

| Term                   | Definition                                                                                                                                                         |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **CitopyOS**           | The operating system used by Citopy devices.                                                                                                                       |
| **AEM**                | **Android Escape Mode**. An emergency recovery environment accessible from the Citopy password recovery screen.                                                    |
| **RTP**                | **Recovery Transfer Protocol**. Citopy's standard computer-assisted recovery system for restoring access to a device and its data.                                 |
| **SQM code**           | The device-specific recovery code supplied with the original Citopy device packaging. It can be used to verify the device during recovery.                         |
| **Security questions** | Recovery questions associated with the device or account that can be used to verify ownership during recovery.                                                     |
| **Storage component**  | A removable or externally linked Citopy storage device that contains or provides access to user data.                                                              |
| **Linked Device**      | A device or component registered with the user's Citopy account and visible through **My Citopy → Linked Devices**.                                                |
| **ForgedPort**         | A last-resort Citopy recovery system that creates a temporary **forged CitopyOS installation** specifically for repairing and recovering a device.                 |
| **Forged CitopyOS**    | The temporary operating system created by ForgedPort. It is designed for recovery operations and is removed after the official CitopyOS installation is completed. |
| **Recovery partition** | A system partition containing the tools and files required to perform recovery operations.                                                                         |
| **Official CitopyOS**  | The normal licensed CitopyOS installation intended for everyday device operation.                                                                                  |

</details>

---

## Contents

* [Recovering phones with forgotten passwords and linked storage components](#recovering-phones-with-forgotten-passwords-and-linked-storage-components)

  * [Android Escape Mode](#1-android-escape-mode)
  * [RTP](#2-rtp)
  * [ForgedPort](#3-forgedport)
* [Recovering data from storage components](#recovering-data-from-storage-components)
* [Recovery method overview](#recovery-method-overview)
* [Additional help](#additional-help)

---

<details>
<summary style="font-size:20px"><strong>Recovering phones with forgotten passwords and linked storage components</strong></summary>

<br>

There are three recovery methods available for Citopy phones.

The recovery methods should be attempted in the following order:

<table>
<thead>
<tr>
<th>Order</th>
<th>Method</th>
<th>Purpose</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>1</strong></td>
<td><strong>Android Escape Mode</strong></td>
<td>First-line recovery, particularly when the original SQM code is available.</td>
</tr>
<tr>
<td><strong>2</strong></td>
<td><strong>RTP</strong></td>
<td>Standard computer-assisted recovery method.</td>
</tr>
<tr>
<td><strong>3</strong></td>
<td><strong>ForgedPort</strong></td>
<td>Last-resort recovery when the normal recovery methods cannot complete the recovery process.</td>
</tr>
</tbody>
</table>

> [!IMPORTANT]
> **Try Android Escape Mode first.** If AEM cannot be used or does not recover the device, proceed to RTP. ForgedPort should only be used when AEM and RTP cannot resolve the problem.

> [!CAUTION]
> **ForgedPort must never be used for a device that has been marked as stolen.** Follow the stolen-device recovery procedure described below.

---

## 1. Android Escape Mode

**Android Escape Mode (AEM)** is Citopy's first-line emergency recovery environment.

AEM is particularly useful when the device's **original SQM code** is available.

### Entering Android Escape Mode

1. Power on the phone.
2. At the password prompt, select **Recover using RTP**.
3. On the recovery screen, press the **RTP logo exactly 14 times**.
4. The device will reboot into Android Escape Mode.

The following recovery mascot will be displayed:

<p align="center">
  <img src="https://bugdroid.org/media/generic/bugdroid-2008-developer.png" width="100" alt="Android recovery mascot">
</p>

5. A prompt will appear requesting the device's original **SQM code**.
6. Enter the SQM code found on the original phone box.
7. The device will restart.
8. When instructed by the recovery environment, remove the required storage component.
9. Reinsert the storage component.
10. Allow the recovery process to complete.
11. The device will restart again.
12. CitopyOS will attempt to restore access to the device's data.

> [!NOTE]
> AEM should be attempted **before RTP** whenever it is available.

> [!WARNING]
> Do not remove the storage component before Android Escape Mode specifically instructs you to do so.

### Stolen-device recovery

If the device has been marked as stolen, **AEM is the permitted recovery method when the original SQM code is available**.

> [!IMPORTANT]
> **Do not use ForgedPort to recover or unlock a device marked as stolen.** If AEM cannot complete recovery of a stolen-marked device, contact Citopy support.

---

## 2. RTP

**RTP (Recovery Transfer Protocol)** is the standard CitopyOS computer-assisted recovery system.

Use RTP when Android Escape Mode cannot be used or does not successfully recover the device.

> [!IMPORTANT]
> Keep **all storage components connected** during the entire RTP recovery process. Disconnecting a component may cause corruption or prevent recovery.

### Requirements

You will need:

* A Citopy phone
* A computer
* A USB-to-USB-C cable capable of data transfer
* Either:

  * The original **SQM code**, or
  * The ability to correctly answer at least **4 security questions**

### Procedure

1. Power on the device.
2. At the password prompt, select **Recover using RTP**.
3. On a computer, open [**rtp.wanets.me/citopy**](https://rtp.wanets.me/citopy).
4. Select **Recover**.
5. Connect the phone to the computer using a data-capable USB-to-USB-C cable.
6. Wait for the phone to appear on the website.
7. Select **Start Recovery Process**.
8. A recovery window containing the Citopy logo and a progress indicator will appear.
9. When prompted, select one of the available verification methods:

   * Enter the **SQM code** found on the original device box.
   * Answer **at least 4 security questions**.
10. Wait for the recovery process to complete.
11. The device will restart.
12. After restarting, CitopyOS will attempt to restore access to the recovered data.

> [!WARNING]
> Do not disconnect the phone or any connected storage components while recovery is running.

> [!IMPORTANT]
> If RTP reports an error that prevents recovery, close the recovery window and browser tab before proceeding to **ForgedPort**.

---

## 3. ForgedPort

> [!CAUTION]
> **ForgedPort is a last-resort recovery method.** Use it only after Android Escape Mode and RTP cannot recover the device.

ForgedPort may be used when:

* Android Escape Mode cannot recover the device.
* RTP repeatedly fails.
* The normal CitopyOS recovery environment cannot complete the recovery process.
* The device has suffered system or recovery corruption that prevents normal recovery.
* A temporary forged CitopyOS environment is required to perform the recovery operation.

> [!IMPORTANT]
> **ForgedPort cannot be used to recover or unlock a device that has been marked as stolen.** Stolen-device recovery must be performed using the appropriate AEM procedure and the original SQM code. If AEM cannot recover the device, contact Citopy support.

### What is ForgedPort?

ForgedPort creates a **temporary forged CitopyOS installation** specifically for the affected device.

The forged installation contains the recovery environment required to access and repair parts of the device that the normal CitopyOS installation cannot access.

The forged OS is temporary and is **not intended for normal operation**.

After recovery is completed, the device is returned to an official CitopyOS installation and the ForgedPort recovery environment is removed.

> [!WARNING]
> ForgedPort modifies system components and may cause permanent data loss. Do not interrupt the recovery process.

> [!IMPORTANT]
> Keep **all storage components connected** throughout the ForgedPort process unless the device specifically instructs you to remove one.

### Procedure

1. On a laptop or PC, open [**rtp.wanets.me/forge**](https://rtp.wanets.me/forge).

2. Select **Forge Citopy Licence**.

3. Select your Citopy device model.

4. If you have the SQM code from the original phone box, enter it.

5. Power on the phone.

6. Connect the phone to the computer using a data-capable USB cable.

7. Select **Detect connection**.

8. Wait for the phone to be detected.

9. Select **Boot ForgedPort**.

10. Wait for the ForgedPort process to finish.

11. Restart the phone.

12. When ForgedPort starts, use the **volume buttons** to navigate and the **power button** to select.

13. Select:

    `Recover device using boot partition`

14. In the next menu, select one of the following:

    `Recover using selected SQM code`

    or

    `Recover using security questions`

15. If you selected the SQM option, enter the selected SQM code.

16. If you selected the security-question option, a keyboard will appear.

17. Answer **at least 4 security questions**.

18. Allow the recovery process to complete.

19. The device will restart.

20. Wait for the **Install Licensed OS** option to appear on the phone.

21. **Do not disconnect the phone from the computer.**

22. Remove the storage component when instructed by the device.

23. On the computer, select **Install Official OS**.

24. On the phone, select **Install Licensed OS**.

25. Wait for the official CitopyOS installation to complete.

26. The phone will boot into the official CitopyOS installation.

27. The **ForgedPort recovery environment will be removed**.

> [!IMPORTANT]
> ForgedPort is temporary. Once the official CitopyOS installation is completed, the forged recovery environment and its recovery partition are deleted.

> [!WARNING]
> Do not power off the phone or computer, disconnect the USB cable, or interrupt the official CitopyOS installation.

</details>

---

<details>
<summary style="font-size:20px"><strong>Recovering data from storage components</strong></summary>

<br>

This procedure is intended for storage components affected by:

* A forgotten component password
* The `invalid.link.method` error
* A component that is physically connected but does not appear under **My Citopy → Linked Devices**

> [!NOTE]
> This recovery procedure is designed to restore access to the storage component without deleting its stored data.

### Procedure

1. Open the **My Citopy** app.
2. Navigate to **Linked Devices**.
3. Check whether the affected storage component appears.
4. If the component does not appear, keep **My Citopy** and the **Linked Devices** section open.
5. Connect the storage component while the section is open.

The component should appear with its **component ID** displayed underneath it.

6. Press the component icon **exactly 23 times**.
7. Wait **2 seconds**.
8. The component will appear in **Linked Devices**.
9. Select the linked component.
10. Select **Recover**.
11. Answer **3 security questions**.
12. If you are unable to answer the required security questions, contact Citopy support through the website provided in the official Citopy GitHub repository.

> [!IMPORTANT]
> The 23-tap sequence only causes the component to appear in the **Linked Devices** interface. It does not bypass the recovery verification.

> [!NOTE]
> This recovery procedure is designed to preserve the data stored on the component.

</details>

---

## Recovery method overview

<table>
<thead>
<tr>
<th>Situation</th>
<th>First option</th>
<th>Next option</th>
</tr>
</thead>
<tbody>
<tr>
<td>Forgotten phone password + original SQM available</td>
<td><strong>Android Escape Mode</strong></td>
<td>RTP if AEM fails</td>
</tr>
<tr>
<td>Forgotten phone password + no SQM</td>
<td><strong>RTP</strong></td>
<td>ForgedPort if normal recovery fails</td>
</tr>
<tr>
<td>AEM fails</td>
<td><strong>RTP</strong></td>
<td>ForgedPort if RTP also fails</td>
</tr>
<tr>
<td>RTP fails</td>
<td><strong>ForgedPort</strong></td>
<td>Contact Citopy support if unsuccessful</td>
</tr>
<tr>
<td>Device marked as stolen + original SQM available</td>
<td><strong>Android Escape Mode</strong></td>
<td>Contact Citopy support if AEM fails</td>
</tr>
<tr>
<td>Device marked as stolen + original SQM unavailable</td>
<td><strong>Contact Citopy support</strong></td>
<td>Do not use ForgedPort</td>
</tr>
<tr>
<td>Storage component missing from Linked Devices</td>
<td><strong>Storage component recovery</strong></td>
<td>Contact Citopy support if unsuccessful</td>
</tr>
<tr>
<td><code>invalid.link.method</code></td>
<td><strong>Storage component recovery</strong></td>
<td>Contact Citopy support if unsuccessful</td>
</tr>
</tbody>
</table>

> [!IMPORTANT]
> **Never use ForgedPort for a stolen-marked device.** If the device is marked as stolen, use AEM with the original SQM code when available. If AEM cannot complete recovery, contact Citopy support.

---

## Additional help

If none of the procedures in this guide resolve the issue, **do not repeatedly attempt recovery operations**.

Repeated modifications to recovery or system partitions may reduce the possibility of successful data recovery.

When contacting Citopy support, provide:

* Device model
* CitopyOS version, if known
* Exact error message
* Recovery method attempted
* Whether the original SQM code is available
* Whether the affected storage component is connected
* Whether the device is detected by the recovery system

<p align="center">
  <strong>Citopy Support</strong><br>
  <sub>Document created by Wanets. Last edited September 28<sup>th</sup> 2026</sub>
</p>
