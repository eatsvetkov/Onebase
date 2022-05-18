# ESP32

# General comands

**Загрузить файл .py на esp32:**

    UPIOT: Put Current File

Открыть UPIOT:

    Ctrl + Alt + M

**Список файлов на esp32:**

    sampy ls

# OpenHAB  & MQTT & ESP32

# Connection OpenHAB to MQTT

## Step 1 - Starting

Connect to openhabian \\192.168.0.100:8080

## Step 2 - Install MQTT Binding

Paper UI - Add-ons - BINDINGS - MQTT Binding (Install)

## Step 3 - Configuration

Inbox - *plus* - MQTT Binding - Add manually - MQTT Broker

**Configuration parameters**
Broker Hostname/IP - 192.168.0.100
Broker Port - 1883
Username - openhabian
Password - openhabian

# Add ThingS

## Step 1 - Starting

Inbox - *plus* - MQTT Binding - Add manually - Generic MQTT Thing

## Step 2 - Choose Bridge Selection

# Add Items

## Step 1 - Creating Items

\\192.168.0.100\openHAB-conf\Items\demo.items
**Structure example:** 

Swich TestMQTT “Checking”


- Swich - Item type
- TestMQTT - variable
- “Checking” - name

## Step 1 - Creating Sitemap

\\192.168.0.100\openHAB-conf\sitemap\demo.sitemap
**Structure example:** 

“itemap demo label="Main Menu"
      {
         Frame {
                     Switch item=TestMQTT
                     }
      }

# Add Channels

## Step 1 - Creating Channel

Configuration - Things - Test MQTT Thing - Channels - *plus*

## Step 2 - Configuration

**Configuration parameters**
Channel type - On/Off swich
Channel id - TestMQTT
MQTT command topic - /TestMQTT/out

    *(TestMQTT - topic, out - subtopic)* 

# Link Channels

\\192.168.0.100\openHAB-conf\Items\demo.items

Swich   TestMQTT                “Checking”                {channel="mqtt:topic:705f4356:TestMQTT"}

# Relay key via ESP32

![](https://paper-attachments.dropbox.com/s_33C732066F6148DC6B8AB7EF8F8A1521C5020C58CD83E336379670DD880F71D8_1588445857175_photo_2020-05-02_21-57-14.jpg)

## Схема подключения катушки реле через NPN транзистор.

**Инфо:** 
Резистор - 400 Ом
Транзистор - S8050 NPN
Катушка - 5VDC

