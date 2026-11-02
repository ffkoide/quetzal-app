# Quetzal

A native Mac viewer for Parquet files — local or on S3.

Open a file, a folder of Parquet files, or an `s3://` object and read it right away. Quetzal reads only the parts it needs (the footer, then the row groups you look at), so a big file — even one in a bucket — opens without being downloaded first.

**Website:** https://ffkoide.github.io/quetzal-app/

## About this repository

This repository is used for **issue tracking, release management and the website**. The application's source code is not published here; Quetzal is not open source for now.

- **Download:** the [releases page](https://github.com/ffkoide/quetzal-app/releases). Each release is a signed and notarized DMG (macOS 14 or later, Apple Silicon and Intel).
- **Bugs and feature requests:** the [issue tracker](https://github.com/ffkoide/quetzal-app/issues).
- **Website:** the `site/` folder, published by GitHub Pages.

## Features

- Opens local files, folders of Parquet files (Hive-style `key=value/` partitions as one table) and S3 objects, with HTTP range requests — nothing is downloaded first
- S3 connections with AWS profiles (including SSO), access keys kept in the Keychain, or anonymous access to public buckets; S3-compatible servers such as MinIO or Cloudflare R2
- Browse buckets and folders like Finder; search below a folder; Quick Open (⌘P) for recent files, connections and indexed keys
- Column explorer: statistics, histogram, box plot, top values; time-series chart with zoom for sensor-style data
- Filter and sort by column; copy as TSV; export to CSV, TSV, JSON Lines or Parquet
- Compare two files or folders: schema and value diff
- Inspector for the file's metadata, row groups and column chunks; a cell pane for long values and JSON
- Quick Look preview and thumbnails in Finder
- A command-line tool (`quetzal`) and an MCP server for AI clients such as Claude Code, read-only

## Requirements

macOS 14 or later. Universal build (Apple Silicon and Intel).

## Status

Not released yet. The first builds will appear on the releases page.

---

Quetzal is a personal project by [ffkoide](https://github.com/ffkoide). Apache Parquet is a trademark of the Apache Software Foundation; Quetzal is not affiliated with it. Mac and macOS are trademarks of Apple Inc.
