# PC-Stress-Test-
This Python script opens infinite XKCD pages. WARNING: USE AT YOUR OWN COST. High probability of Desktop Window Manager (DWM) white-screen reset. ALWAYS SAVE YOUR WORK BEFORE TESTING. DO NOT ASSUME A POWERFULL SYSTEM CAN HANDLE THIS. RUNNING THIS SCRIPT CONSUMES LARGE AMOUNTS OF RAM.

A lightweight Python Proof of Concept (PoC) designed to test Windows Desktop Window Manager (DWM) process limits, browser session recovery, and OS handle exhaustion under rapid subprocess creation.

---

## ⚖️ LEGAL DISCLAIMER & TERMS OF USE

**PLEASE READ THIS DISCLAIMER CAREFULLY BEFORE USING OR EXECUTING THIS SOFTWARE.**

1. **NO WARRANTY (PROVIDED "AS IS"):** THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDER "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED.
2. **LIMITATION OF LIABILITY:** IN NO EVENT SHALL THE AUTHOR OR COPYRIGHT HOLDERS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, LOSS OF DATA, SYSTEM CRASHES, HARDWARE OVERHEATING, OR DESKTOP COMPOSITOR FAILURE) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE.
3. **ASSUMPTION OF RISK:** BY DOWNLOADING, CLONING, OR EXECUTING THIS SCRIPT, YOU EXPRESSLY ACKNOWLEDGE THAT THIS SOFTWARE IS DESIGNED TO INTENTIONALLY EXHAUST OS RESOURCES. YOU ASSUME 100% OF THE RISK AND RESPONSIBILITY FOR ANY SYSTEM INSTABILITY OR DATA LOSS THAT MAY OCCUR.
4. **BENCHMARK & EDUCATIONAL USE ONLY:** THIS TOOL IS INTENDED STRICTLY FOR EDUCATIONAL PURPOSES, SYSTEM RESOURCE BENCHMARKING, AND OS STRESS TESTING IN CONTROLLED ENVIRONMENTS.

---

## 🚨 SYSTEM INSTABILITY WARNING

> **WARNING:** Running this script triggers an infinite loop of browser tab initializations via Python's `antigravity` module and `importlib.reload()`. 

Executing this code will rapidly consume system memory, process handles, and desktop compositor threads. **Expected side effects include:**
* Unresponsive desktop or frozen windows.
* Desktop Window Manager (`dwm.exe`) crash resulting in a white or blank screen.
* Web browser collapse or infinite crash recovery prompts.

**Save all working documents and close sensitive applications before running.**

---

## 🛠️ How It Works

The script bypasses Python's module import caching via `importlib.reload()`, continually forcing the OS default browser to fetch the built-in `antigravity` easter-egg URL (`https://xkcd.com/353/`) in rapid succession until process limits are reached.

### Execution
```bash
python main.py
