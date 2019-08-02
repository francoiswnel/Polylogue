# Polylogue

Polylogue is a polyphonic analogue synthesizer written in Pure Data for the [Critter & Guitari Organelle](https://www.critterandguitari.com/organelle), inspired by the workflow of the [Korg Monologue](https://www.korg.com/us/products/synthesizers/monologue/) and the [Korg Volca Keys](https://www.korg.com/us/products/dj/volca_keys/).

# Features

* Six voice polyphony with two oscillators per voice.
* Each voice is fully articulated, featuring its own envelope generator, low-frequency oscillator, filter, and amplifier.
* Five wave shapes per oscillator: Saw, triangle, square, cosine, and noise.
* Pulse width modulation through an adjustable duty cycle for the square wave oscillators.
* A resonant filter which self-oscillates.
* ADSR-style envelope generator which can simultaneously target the amplifier, both oscillator pitches, and the filter cutoff.
* Per-voice low-frequency oscillator with saw, triangle, square, and cosine wave shapes, which can simultaneously modulate both oscillator pitches and the filter cutoff.
* The secondary oscillator can be offset up to two octaves up and down from the primary oscillator, as well as detuned about another two-thirds of an octave up and down.
* Four channel mixer for adjusting the levels of the two oscillators, line in, and a feedback loop drive.
* Sequencing with Critter & Guitari's Sequencer 2.

# Download

Download the latest release:

* [Patch Storage](url)
* [GitHub](url)

Installation instructions:

1. Copy the `Polylogue.zop` file to your patches directory on your SD card or USB drive.
2. From the Organelle menu, reload the storage.
3. Navigate to the patch and select `Install Polylogue`.

# Discussion

Please leave feedback or ask questions in the [Critter & Guitari forum thread](url), or [create an issue](url) on GitHub.

# Menu Guide

Page 1: VCO 1

1. Wave: 0. Saw, 1. Triangle, 2. Square, 3. Cosine, 4. Noise.
2. Shape: Square wave duty cycle.
3. Octave: Keyboard transpose, -3 to +1 octaves.

Page 2: VCO 2

1. Wave: 0. Saw, 1. Triangle, 2. Square, 3. Cosine, 4. Noise.
2. Shape: Square wave duty cycle.
3. Octave: Offset from VCO 1, -2 to +2 octaves.
4. Detune: Continuous pitch adjustment.

Page 3: Mix

1. VCO 1
2. VCO 2
3. Line In
4. Drive

Page 4: VCF

1. Cutoff: High-pass filter with a peak frequency ranging from 100 to 5000 Hz.
2. Resonance: Unstable and self-oscillating above about 90%.

Page 5: EG

1. Attack: Ramp up to peak volume over 0-5000 ms.
2. Decay: Ramp down to sustain volume over 0-5000 ms.
3. Sustain: Percentage of peak volume.
4. Release: Ramp down to zero volume over 0-5000 ms after releasing the note.

Page 6: EG Targets

1. VCO 1 Pitch: Modulate the pitch of the primary oscillator.
2. VCO 2 Pitch: Modulate the pitch of the secondary oscillator.
3. VCF Cutoff: Modulate the cutoff frequency of the filter.
4. VCA: Modulate the output of the voice.

Page 7: LFO

1. Wave: 0. Saw, 1. Triangle, 2. Square, 3. Cosine.
2. Rate: 0 to 20 Hz.

Page 8: LFO Targets

1. VCO 1 Pitch: Modulate the pitch of the primary oscillator.
2. VCO 2 Pitch: Modulate the pitch of the secondary oscillator.
3. VCF Cutoff: Modulate the cutoff frequency of the filter.

Page 9: Utility

1. Pitch Scale: Adjust the scale of the pitch target knobs.

# Pure Data Screenshots

Main:

![main.pd](url)

Voice:

![voice.pd](url)

VCO 1:

![vco1.pd](url)

VCO 2:

![vco2.pd](url)

VCO:

![vco.pd](url)

Saw Wave:

![saw.pd](url)

Triangle Wave:

![triangle.pd](url)

Square Wave:

![square.pd](url)

EG:

![eg.pd](url)

LFO:

![lfo.pd](url)

VCF:

![vcf.pd](url)

Mixer:

![mixer.pd](url)
