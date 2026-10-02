# Big Reactors Control (ComputerCraft 1.63)

Runs an actively cooled Big Reactors 0.3.4 reactor and its turbines from one computer, with a
dashboard on up to 4 advanced monitors.

- **Control rods** are set so the reactor makes exactly the steam the running turbines use.
- **Turbines** spin up with their coils off, then run with coils on at full steam (2,000 mB/t).
- **Load following:** when the turbines' power buffers fill up, turbines stand down one at a time
  and come back when the power is needed.
- **Steam limit:** one reactor can boil at most 50,000 mB/t (25 turbines). Extra turbines are kept
  as spares so the rest get full steam.
- **Dashboard:** reactor status, rods, steam, water, temperatures, fuel, total RF/t, RF per ingot,
  a power graph, every turbine, and any tanks you connect (water and steam storage).

It's light on the server: wired peripherals only, no rednet, and the monitors only redraw what
changed. With 4 turbines it makes about 10 calls a second in all.

## What you need

- An advanced computer, and 1 to 4 **advanced monitors** (8 x 5 each works well). The first monitor
  shows the overview and the others show the turbines.
- A **Computer Port** on the reactor and on every turbine.
- **Wired modems** and **networking cable**: a modem on the computer, on each Computer Port, each
  monitor and each tank you want on the dashboard. Right-click each modem so it turns red.
- Two facing turbines can't share one modem block: move one of the pair's Computer Port up a
  layer.

## Installing

With your `get` program on the computer:

```
get https://raw.githubusercontent.com/landonracer109/BigReactors-CC/<commit>/brcontrol startup
```

Then reboot the computer (hold Ctrl+R). It starts by itself on every boot. Fill the water loop
before the first start.

## Settings

At the top of the file: turbine flow, the RPM where coils switch on and off, buffer levels for
standing turbines down, update times, text size (`textScale`, 0 = the biggest that fits) and `monitorOrder` (put the monitor names in the
order you want; each monitor shows its name in the bottom-left corner).

Press **Q** on the computer to stop the program (the rods stay where they are).
