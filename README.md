# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),

## [1.0.15] - Multi-Driver Update
### Added
- Fast reconnect, redirect support and connection timeout parameter in ORB Multi Driver
- Parameter for permanent redirect handling
- Connection timeout setting

### Fixed
- ORB Driver auto-reconnect logic
- NoVideo state and timestamp handling on ORB Multi Driver
- Event handler disposal issues
- Auto-restart when stream is disconnected
- Separate audio URL handling
- Audio starting issues on video client
- Release date in build artifacts

### Changed
- Incremented release date for upcoming build

## [1.0.14] - 2025-10-16 - New Ingest Protocols
### Added
- Support for new ingest protocols (RTSP libraries overhaul)
- Reconnect to stream when transcode-audio or generate-timestamp settings change from Mission Control
- Connection timeout setting

### Fixed
- Auto-restart when driver disconnects
- Audio transcoding issues (multiple fixes)
- Audio starting problems on video client
- Separate audio URL handling
- Driver process disposal when hardware is disabled from Mission Control
- Timestamp generation for RTP streams (disabled orbv-generate-timestamps when not needed)

### Removed
- Auto-reconnect (temporarily removed then re-implemented better in 1.0.15)
- NALUnit combiner (no longer required with new libraries)

### Changed
- Better audio header handling

## [1.0.13] - 2025-07-10 - Area Zoom and Audio Transcoding
### Added
- Area Zoom (CenterAndZoomToRectangle) using OnvifNormalizedRectangle
- PTZ throttling and improved PTZ manager (removed unnecessary locks)
- Zoom support in PTZMoveStep
- Various PTZ improvements (ongoing work)

### Fixed
- PTZ manager locking issues
- Serialization of PTZ direction
- Hardcoded HTTP → HTTPS in URLs

### Changed
- Default Streaming Engine port modified

## [1.0.12] - 2025-05-08 - SRT PTZ and Metadata
### Added
- Full PTZ control over SRT
- PTZ commands forwarded to Streaming Engine
- TCP RTSP PING keep-alive
- Timestamp overlay options
- No timeout on RTSP sessions
- Image rotation support (single & multi driver)
- ImageProvider fixes per channel in multi-driver

### Fixed
- PTZ command logging improvements
- Various ONVIF fixes and testing
- Constants and serialization issues

### Changed
- Applied newer ORBV libraries
- Started multi-driver adaptations

## [1.0.11] - 2025-02-XX (unreleased intermediate builds)
### Added
- i-PRO PTZ support
- Opus audio testing
- More detailed PTZ command logging
- TCP server option for ASCII metadata overlays (backported from 1.0.4)

### Fixed
- Audio adjustments for various sources
- ONVIF constant issues

### Removed
- Skydio-specific code (temporary)

## [1.0.10] - 2025-01-21 - Skydio Update (dev build)
### Added
- Skydio integration updates
- SourceFactory for URI-based ingest
- Multi-driver image provider improvements
- Image rotation in single driver

### Fixed
- Multi-driver logging issues
- Queue empty bugs
- Password leakage in URL logs

## [1.0.9] - 2024-03-17 - Remote Retrieve Fix
### Fixed
- Remote Retrieval licensing removal
- Queue empty / sample queue disposal issues
- Passwords no longer logged in URLs
- Network reconnection issues
- Reset media type on keyframe
- Reset parameters on NULL frames

### Security
- Removed vulnerable dependencies

## [1.0.5] - DEV / Transcoding Builds

- Changed: Using new RTSP Librairies
- Removed: RTMP protocol. ORB Driver connects to Streaming Engine to get RTSP from RTMP feeds.

## [1.0.4] - 23.07.2022

- Added: AAC Audio Support for Streaming Engine RTMP Proxy
- Added: TCP Server as an option to receive ASCII data for metadata overlays
- Fixed: AAC Audio from OBS, DJI and various cameras are working properly
- Changed: Metadata colors in RGBA format
- Changed: Metadata timeout in minutes
- Changed: Renamed metadata settings



