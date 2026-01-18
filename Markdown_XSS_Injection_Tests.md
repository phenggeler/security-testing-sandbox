# Markdown XSS & HTML Injection Test Patterns

**Purpose:** Testing GitHub's markdown sanitization - inspired by PayloadsAllTheThings

**Warning:** This file contains XSS payloads for security testing purposes only.

---

## Test 1: Basic Script Tag

<script>alert('XSS-1')</script>

## Test 2: IMG Tag with onerror

<img src=x onerror=alert('XSS-2')>

## Test 3: SVG with onload

<svg onload=alert('XSS-3')>

## Test 4: Javascript URL in Link

[Click me](javascript:alert('XSS-4'))

## Test 5: iframe Injection

<iframe src="javascript:alert('XSS-5')"></iframe>iframe>

## Test 6: Style Tag

<style>body{background:url("javascript:alert('XSS-6')")}</style>

## Test 7: HTML Event Handlers

<div onclick="alert('XSS-7')">Click me</div>div>

## Test 8: SVG foreignObject

<svg><foreignObject><iframe src="javascript:alert('XSS-8')"></iframe></foreignObject></svg>

## Expected Results

If GitHub's markdown sanitizer is working correctly, ALL of the above payloads should be neutralized.</script>
