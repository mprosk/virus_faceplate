# Access Virus TI2 Vocoder Faceplate

When using the vocoder built into the Virus TI series synthesizer, the knobs and buttons of the filter section are replaced with vocoder-specific functions. This faceplate slides over the filter section, providing legends and references when using the vocoder.

PDF versions are included for creating printed versions at home. Some trial-and-error for correct scaling may be required.

![render](https://github.com/mprosk/virus_faceplate/blob/main/img/render.png)



![irl](https://github.com/mprosk/virus_faceplate/blob/main/img/irl.jpg)



# Vocoder Documentation

> *The following information is copied from the Access's documentation on the Virus vocoder. It is included here for reference*.

Although available as "effect", the Virus Vocoder actually replaces the entire filter section i.e. Vocoder and normal filters cannot be used at the same time within a single program.

The Virus vocoder has two banks of up to 32 bandpass filters: One to analyze the frequency spectrum of a modulator audio signal, and the other to process a carrier signal (usually the internal oscillators) accordingly.

#### Mode

| Carrier Signal     | Meaning                                                      |
| ------------------ | ------------------------------------------------------------ |
| Off                | The Vocoder is disabled, no other Vocoder parameters will be visible. |
| Oscillator         | The carrier is the entire oscillator section, including any noise. |
| Osc Hold           | Identical to "Osc" except that Hold mode is activated for the vocoder. |
| Noise              | The carrier is the noise signal only. The rest of the oscillator section is disabled |
| In L, In L+R, In R | The carrier is one or both of the audio inputs.              |

#### Spread

-64 to +63: Simultaneously controls Carrier Spread and Modulator Spread (see below).	

#### Q-Factor

-64 to +63: Simultaneously controls Carrier Q and Mod Q (see below), overriding those two parameters.

*Only available if both filter SELECT buttons are active.*

#### Carrier Spread

-64 to +63: How far apart individual Carrier bands are. The standard value is +63 (100% i.e. full range), negative values effectively invert the order of bands - great for special effects.

*Modulation destination "Filter1 Key Follow".*

#### Carrier Q

0 to 127: Quality (steepness) of the Carrier bands.

*Modulation destination "Filter1 Resonance".*

#### Modulator Spread

-64 to +63: How far apart individual Modulator bands are. The standard value is +63 (full range), negative values effectively invert the order of bands.

*Modulation destination "Filter2 Key Follow".*

#### Mod Q

0 to 127: Quality (steepness) of the Modulator bands.

*Modulation destination "Filter2 Resonance".*

#### Center Freq

-64 to +63: Centre frequency of the Carrier bank.

*Modulation destination "Filter1 Cutoff".*

#### Balance

-64 to +63: Balance between the carrier and modulator signals. For pure vocoder signal, set this value to <0>.

*Modulation destination "Filter Balance".*

#### Mod Offset

-64 to +63: Centre frequency offset of the modulator bank relative to the carrier bank.

*Modulation destination "Filter2 Cutoff".*

#### Carrier Attack

0 to 127: Attack time of the carrier’s own “envelope follower”. Together with Carrier Release, this is used to smoothen the vocoded signal.

#### Carrier Release

0 to 127: Release time of the carrier’s envelope follower. Together with Carrier Attack, this is used to smoothen the vocoded signal.

#### Spectral Balance

0 to 127: Balance between high and low frequencies in the vocoded signal. In effect, this parameter works like a simple equalizer, determining the overall color of the vocoder output. Higher values can improve the clarity of speech. 

*Modulation destination "Filter Env Slope".*

#### Bands

1 to 32: The number of filter bands used. The higher this number, the higher the quality (e.g. speech becomes more intelligible). Lower values are better for robot voices etc.

*Modulation destination "Filter Env Release".*

## Vocoder Parameters on Mod Matrix

| Vocoder Parameter | Modulation Destination |
| ----------------- | ---------------------- |
| Carrier Freq      | Cutoff 1               |
| Mod Freq Offset   | Cutoff 2               |
| Carrier Q         | Filter 1 Resonance     |
| Modulator Q       | Filter 2 Resonance     |
| Q Factor          | Filter 1 Resonance     |
| Carrier Spread    | Filter 1 Key Follow    |
| Modulator Spread  | Filter 2 Key Follow    |
| Spread            | Filter 1 Key Follow    |
| Carrier Attack    | Filter Env Attack      |
| Carrier Release   | Filter Env Decay       |
| Spectral Balance  | Filter Env Slope       |
| Bands             | Filter Env Release     |
| Balance           | Filter Balance         |
