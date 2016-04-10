# logicshell - logic circuits created using C and bash
![TransistorShell](transistor.png)

## What is logicshell?

Logicshell is a project that grew out of a conversation on logic circuits with a friend. It all started when we wondered if it would be possible to simulate a simple logic circuit using operating system tools only.

## How can we build this?

First, we must view the most fundamental features of our logic circuit: **electrons** and **current**. Suppose the **null-byte** is an electron. Then, `/dev/zero` provides an infinite supply of electrons and `/dev/null` a supply of holes (virtual positively charged particles). Let's call these devices `Vss` and `Vdd`, respectively.

In our project we use a unix pipe as a `wire`, that is, a conductor with parasitic capacitance. If the `wire` is connected to `Vss`, its pipe buffer in kernel space quickly fills up with null-bytes, and the `wire` acts like a negatively charged metal plate. If it is connected to `Vdd`, the pipe buffer is drained, and the `wire` acts like a positively charged metal plate.

`Wires` may thus carry *logic signals*: A `wire` that is filled with null-bytes corresponds to a *logic zero*, and a `wire` that is completely empty corresponds to a *logic one*. A `wire` that contains some null-bytes, but is neither full nor empty, corresponds to an undefined voltage, and will act as a *logic one* or a *logic zero* depending upon how we measure it.

## Transistors

Coming soon.
