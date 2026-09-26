# Thaura AI – Technical Testing Assessment

## Overview

This repository contains my Software Quality Assurance (SQA) technical testing assessment for Thaura AI. The assessment focuses on functional testing, API testing, performance testing, security testing, and AI-related evaluation tasks.

---

## Tester Information

**Name:** Afrina Sultana

**Role:** Software Quality Assurance Engineer

**Tools Used:**
- Google Chrome DevTools
- Microsoft Edge DevTools
- Postman
- Apache JMeter
- Lighthouse
- Git & GitHub
- Microsoft Excel

---

# Task 01 – Thaura Web Application Testing

## Scope Covered

### Authentication & Session Management
- Login using newly created account
- Token expiration validation
- Concurrent session behavior
- Logout invalidation testing

### Free Tier Validation
- Free-tier message limit (5 messages / 2 hours)
- Fixed window validation
- Failed response quota consumption
- Limit bypass testing:
  - Multiple tabs
  - Session refresh
  - Direct API usage

### File Upload Testing
- PDF upload and extraction validation
- Spreadsheet upload and extraction validation
- Image upload and OCR validation
- Corrupted file handling
- Password-protected file handling
- Empty file handling
- Oversized file handling
- Cross-session file isolation

### Memory & Incognito Testing
- Memory persistence across chats
- Built-in Incognito Mode isolation
- Chat history isolation
- Memory leakage verification

### Developer API Testing
- Required parameter validation
- Optional parameter validation
- Invalid data type validation
- Temperature boundary validation
- max_completion_tokens limit validation
- max_tokens vs max_completion_tokens precedence
- Authentication & authorization testing
- Missing API key validation
- Invalid API key validation
- Malformed API key validation
- Zero-balance API key validation
- Streaming response validation
- Non-streaming response validation
- Usage token accounting validation

### Negative & Boundary Testing
- Blank submissions
- Invalid email formats
- Invalid password formats
- Maximum field length validation
- Invalid file type validation
- Settings page validation
- Account page validation
- Billing page validation
- Special character input validation
- Long string input validation

---

## Task 01 Summary

| Metric | Result |
|----------|----------|
| Total Test Cases | 35 |
| Passed | 35 |
| Failed | 0 |
| Pass Rate | 100% |
| Defects Logged | 1 |

---

# Task 02 – Website Technical Testing

## Functional & Data Correctness Testing

### Link Validation
- Internal links
- External links
- HTTP status verification
- Redirect validation
- HTTPS validation

### Contact Form Testing
- Required field validation
- Email validation
- Field length validation
- Submission verification
- Error handling validation

### Pricing Validation
- Monthly pricing verification
- Annual pricing verification
- Discount calculation verification
- Cross-page pricing consistency validation

### Content Consistency Testing
- Technical claim consistency
- Feature consistency
- Documentation consistency

---

## Performance Testing

### Lighthouse Audits
Performed on:
- Home Page
- Pricing Page
- API Documentation Page
- FAQ Page

Collected:
- Performance Score
- Best Practices Score
- SEO Score
- LCP
- CLS
- INP/FID
- TTFB

### Load Testing
Performed using Apache JMeter:
- Home Page
- Pricing Page
- API Page
- FAQ Page

### Asset Optimization Testing
- Image format validation
- Video optimization validation
- Compression validation
- Lazy loading validation

### Monitoring
- JavaScript console monitoring
- Network request monitoring
- Failed request analysis

---

## Security Testing

### HTTPS Validation
- HTTPS enforcement verification
- Mixed content validation

### Security Header Validation
- Content-Security-Policy
- X-Frame-Options
- Strict-Transport-Security
- X-Content-Type-Options

### Input Validation Testing
- Long strings
- Script-like input
- Unicode input
- RTL text input

### Sensitive Information Exposure Testing
- Page source review
- Console log review
- Network response review

### Cookie Security Validation
- Secure attribute
- HttpOnly attribute
- SameSite attribute

---

## Task 02 Summary

| Metric | Result |
|----------|----------|
| Total Test Cases | 44 |
| Passed | 44 |
| Failed | 0 |
| Pass Rate | 100% |

---

# Task 03 – AI & Software Testing Questions

Topics Covered:

1. Impact of AI on software testing in the next 2–3 years
2. Personal use of AI in testing activities
3. AI tools currently used
4. Most useful AI tool for software testing

---

# Defects Found

## BUG-001
**Title:** Invalid email is accepted and validated only after proceeding to the next onboarding step.

**Severity:** Medium

**Description:**
The application allows a user to continue with an invalid email address and only displays the validation error after progressing to the next onboarding screen.

---

# Repository Structure

```text
Thaura-AI-Technical-Testing/
│
├── README.md
│
├── Task-01-Web-App-Testing/
│   ├── Test-Report/
│   ├── Screenshots/
│
├── Task-02-Website-Technical-Testing/
│   ├── Test-Report/
│   ├── Screenshots/
│   └── JMeter/
│
├── Task-03-AI-Questions/
│   └── Task 03 AI & Testing — Reflection Questions
│
├── Bug-Reports/
│   └── Bug_Report.xlsx
```

---

# Testing Limitations

- Testing was conducted from the client side only.
- Backend implementation and database operations could not be independently verified.
- Server-side deletion and storage behavior could not be validated without backend access.
- Results are based on observable application behavior, API responses, browser developer tools, Lighthouse audits, and JMeter execution results.

---

# Conclusion

The assessment covered functional testing, API testing, performance testing, security testing, and AI-related evaluation tasks. Most tested functionality behaved according to the documented requirements. One medium-severity validation issue was identified and documented separately in the bug report.