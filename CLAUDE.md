# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a simple educational web application for teaching Chinese character writing and pronunciation to children. It's a single HTML file (`3-汉字笔画拼音学习.html`) that creates an interactive learning experience with stroke animation, pinyin display, and voice synthesis.

## Architecture

- **Single-file application**: All HTML, CSS, and JavaScript contained in one file
- **CDN dependencies**: Uses external libraries loaded via CDN (requires internet connection)
- **No build process**: Direct browser execution, no compilation or bundling needed

## Key Dependencies

- **Hanzi Writer** (v3.5): Stroke animation and character rendering - loaded from jsDelivr CDN
- **pinyin-pro**: Pinyin conversion with tone marks - loaded from unpkg CDN
- **Web Speech API**: Browser-native voice synthesis for character pronunciation

## Core Functionality

1. **Character Input**: Single Chinese character input with validation
2. **Pinyin Display**: Automatic pinyin generation with proper tone marks
3. **Stroke Animation**: Interactive character writing demonstration using Hanzi Writer
4. **Voice Pronunciation**: Text-to-speech using browser's native speech synthesis
5. **Practice Grid**: Tian-zi-ge (田字格) writing grid for proper character formation

## Development Commands

Since this is a static HTML file with no build process:

- **Run locally**: Open `3-汉字笔画拼音学习.html` directly in a web browser
- **Test**: Manual testing in browser - no automated test framework
- **Deploy**: Host the single HTML file on any static web server

## Code Structure

The file is organized into three main sections:
- **HTML** (lines 156-179): UI structure with input, display, and control elements
- **CSS** (lines 12-154): Styling using CSS custom properties for theming
- **JavaScript** (lines 180-265): Core functionality including character loading, animation, and speech

## Key Functions

- `loadCharacter()`: Main function that validates input, generates pinyin, and initializes Hanzi Writer
- `animateStroke()`: Triggers stroke animation replay
- `speak()`: Uses Web Speech API to pronounce the character

## Important Considerations

- **Character validation**: Uses regex `/[\u4e00-\u9fa5]/` to ensure only Chinese characters
- **Internet dependency**: Requires CDN access for Hanzi Writer data files
- **Browser compatibility**: Uses modern features like CSS Grid and Web Speech API
- **Child-friendly design**: Slow speech rate (0.8) and visual feedback for learning