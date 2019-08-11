# Polylogue

Polylogue is a polyphonic analogue synthesizer written in Pure Data for the [Critter & Guitari Organelle](https://www.critterandguitari.com/organelle), inspired by the workflows of the [Korg Monologue](https://www.korg.com/us/products/synthesizers/monologue/) and the [Korg Volca Keys](https://www.korg.com/us/products/dj/volca_keys/).

# Features

* Six voice polyphony on the Organelle M, and four voice polyphony on the Organelle 1, with two oscillators per voice.
* Each voice is fully articulated, featuring its own envelope generator, low-frequency oscillator, filter, and amplifier.
* Five wave shapes per oscillator: Saw, triangle, square, cosine, and noise.
* Pulse width modulation through an adjustable duty cycle for the square wave oscillators.
* A resonant filter which self-oscillates.
* ADSR-style envelope generator which can simultaneously target the amplifier, both oscillator pitches, and the filter cutoff.
* Per-voice low-frequency oscillator with saw, triangle, square, and cosine wave shapes, which can simultaneously modulate both oscillator pitches and the filter cutoff.
* The secondary oscillator can be offset up to two octaves up and down from the primary oscillator, as well as detuned about another two-thirds of an octave up and down.
* Four channel mixer for adjusting the levels of the two oscillators, line in, and a feedback loop drive.
* Sequencing with Critter & Guitari's Sequencer 3.
* Polyphonic portamento.

# Download

Download the latest release:

* [Patch Storage](https://patchstorage.com/polylogue/)
* [GitHub](https://github.com/francoiswnel/Polylogue/releases/latest)

Installation instructions:

1. Copy the `Polylogue.zop` file to your patches directory on your SD card or USB drive.
2. From the Organelle menu, reload the storage.
3. Navigate to the patch and select `Install Polylogue.zop`.

# Discussion

Please leave feedback or ask questions in the [Critter & Guitari forum thread](https://forum.critterandguitari.com/t/polylogue-polyphonic-analogue-synthesizer/4725), or [create an issue](https://github.com/francoiswnel/Polylogue/issues) on GitHub.

# Menu Guide

1. VCO 1

    1. Wave: 0. Saw, 1. Triangle, 2. Square, 3. Cosine, 4. Noise.
    2. Shape: Square wave duty cycle.
    3. Octave: Keyboard transpose, -3 to +1 octaves.

2. VCO 2

    1. Wave: 0. Saw, 1. Triangle, 2. Square, 3. Cosine, 4. Noise.
    2. Shape: Square wave duty cycle.
    3. Octave: Offset from VCO 1, -2 to +2 octaves.
    4. Detune: Continuous pitch adjustment.

3. Mix

    1. VCO 1
    2. VCO 2
    3. Line In: Audio input mixed in between the VCOs and the filter stages.
    4. Drive: Audio output mixed in between the VCOs and the filter stages.

4. VCF

    1. Cutoff: High-pass filter with a peak frequency ranging from 100 to 5000 Hz.
    2. Resonance: Unstable and self-oscillating above about 90%.

5. EG

    1. Attack: Ramp up to peak volume over 0-5000 ms.
    2. Decay: Ramp down to sustain volume over 0-5000 ms.
    3. Sustain: Percentage of peak volume.
    4. Release: Ramp down to zero volume over 0-5000 ms after releasing the note.

6. EG Target

    1. VCO 1 Pitch: Modulate the pitch of the primary oscillator.
    2. VCO 2 Pitch: Modulate the pitch of the secondary oscillator.
    3. VCF Cutoff: Modulate the cutoff frequency of the filter.
    4. VCA: Modulate the output of the voice.

7. LFO

    1. Wave: 0. Saw, 1. Triangle, 2. Square, 3. Cosine.
    2. Rate: 0 to 20 Hz.

8. LFO Target

    1. VCO 1 Pitch: Modulate the pitch of the primary oscillator.
    2. VCO 2 Pitch: Modulate the pitch of the secondary oscillator.
    3. VCF Cutoff: Modulate the cutoff frequency of the filter.

9. Config

    1. Portamento: Adjust the note glide time. Turns off at 0%.
    2. Pitch Scale: Adjust the scale of the pitch target knobs.

# Credits

* KontrolModule by [Mark Harris aka TheTechnobear](https://github.com/TheTechnobear).
* Sequencer 3 by Critter & Guitari.
* ADSR from the [clds](https://patchstorage.com/clds/) port by Mark Harris.

# Pure Data Screenshots

Main:

![main.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/main.png)

Voice:

![voice.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/voice.png)

VCO 1:

![vco1.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/vco1.png)

VCO 2:

![vco2.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/vco2.png)

VCO:

![vco.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/vco.png)

Saw Wave:

![saw.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/saw.png)

Triangle Wave:

![triangle.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/triangle.png)

Square Wave:

![square.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/square.png)

Portamento:

![portamento.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/portamento.png)

EG:

![eg.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/eg.png)

LFO:

![lfo.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/lfo.png)

VCF:

![vcf.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/vcf.png)

Mixer:

![mixer.pd](https://raw.githubusercontent.com/francoiswnel/Polylogue/master/Screenshots/mixer.png)
