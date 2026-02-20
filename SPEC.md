# Prudential Insurance Questionnaire - Lead Generation Funnel

## 1. Project Overview

- **Project Name:** Prudential Insurance Questionnaire
- **Type:** Single-page Interactive Web Application
- **Core Functionality:** Multi-step lead generation form for insurance consultation booking
- **Target Users:** Indonesian prospects interested in Prudential insurance products

## 2. UI/UX Specification

### Layout Structure

- **Container:** Centered card (max-width: 480px) with generous padding
- **Header:** Progress bar with 5 steps (rainbow gradient)
- **Content Area:** Question text + selection options
- **Footer:** Navigation button (Lanjutkan/Kembali)

### Responsive Breakpoints

- **Mobile (default):** Full width with 16px padding
- **Tablet/Desktop:** Centered card with max-width 480px

### Visual Design

#### Color Palette

| Element                  | Color       | Hex Code  |
| ------------------------ | ----------- | --------- |
| Primary (Prudential Red) | Red         | `#ED1B2E` |
| Primary Hover            | Dark Red    | `#C41224` |
| Background               | Off-White   | `#FAFAFA` |
| Card Background          | White       | `#FFFFFF` |
| Text Primary             | Dark Gray   | `#1A1A1A` |
| Text Secondary           | Medium Gray | `#666666` |
| Border                   | Light Gray  | `#E5E5E5` |
| Progress Active 1        | Orange      | `#FF6B35` |
| Progress Active 2        | Red         | `#ED1B2E` |
| Progress Active 3        | Pink        | `#E91E8C` |
| Progress Active 4        | Purple      | `#8E44AD` |
| Progress Inactive        | Light Gray  | `#E5E5E5` |

#### Typography

- **Font Family:** 'Inter', sans-serif (Google Fonts)
- **Question Text:** 20px, font-weight 600, line-height 1.4
- **Option Text:** 16px, font-weight 500
- **Button Text:** 16px, font-weight 600

#### Spacing System

- **Card Padding:** 32px (mobile: 24px)
- **Question Margin Bottom:** 32px
- **Options Gap:** 12px
- **Button Margin Top:** 40px

#### Visual Effects

- **Card Shadow:** `0 25px 50px -12px rgba(0, 0, 0, 0.08)`
- **Option Hover:** Background `#F8F9FA`, border color change
- **Option Selected:** Border `#ED1B2E`, background `#FFF5F5`
- **Button Shadow:** `0 4px 14px rgba(237, 27, 46, 0.3)`
- **Transitions:** All 200ms ease-in-out

### Components

#### Progress Bar

- 5 segments, each 20% width
- Active segments: gradient from orange → red → pink → purple
- Inactive segments: light gray
- Rounded ends (border-radius: 4px)
- Height: 4px
- Gap between segments: 4px

#### Question Card

- White background
- Border-radius: 24px
- Drop shadow on card

#### Option Buttons

- Full width
- Border: 2px solid #E5E5E5
- Border-radius: 16px
- Padding: 16px 20px
- States:
  - Default: White background, gray border
  - Hover: Light gray background (#F8F9FA), darker border
  - Selected: Light red background (#FFF5F5), red border (#ED1B2E), red checkmark

#### Navigation Buttons

- **Lanjutkan (Continue):**
  - Full width
  - Background: #ED1B2E
  - Text: White
  - Border-radius: 16px
  - Padding: 18px
  - Hover: Darker red with shadow
- **Kembali (Back):**
  - Text button style
  - Gray text (#666666)
  - No background
  - Appears from step 2 onwards

### Steps & Content

#### Step 1: Kebutuhan (Protection Type)

- Question: "Apa jenis proteksi asuransi yang anda butuhkan saat ini?"
- Options:
  1. Asuransi Kesehatan
  2. Asuransi Jiwa
  3. Asuransi yang dikaitkan dengan investasi (Unit Link)

#### Step 2: Anggaran (Budget)

- Question: "Berapa budget bulanan yang anda alokasikan untuk proteksi keluarga?"
- Options:
  1. Kurang dari Rp 500.000
  2. Rp 500.000 - Rp 1.000.000
  3. Rp 1.000.000 - Rp 2.000.000
  4. Rp 2.000.000 - Rp 5.000.000
  5. Lebih dari Rp 5.000.000

#### Step 3: Waktu Hari (Day Preference)

- Question: "Kapan waktu yang lebih nyaman untuk anda?"
- Options:
  1. Weekdays (Senin-Jumat)
  2. Weekend (Sabtu-Minggu)

#### Step 4: Waktu Jam (Time Slot)

- Question: "Pilih jam operasional yang tersedia?"
- Options:
  1. 09.00 - 11.00 WIB
  2. 11.00 - 13.00 WIB
  3. 13.00 - 15.00 WIB
  4. 15.00 - 17.00 WIB
  5. 17.00 - 19.00 WIB

#### Step 5: Lokasi (Meeting Place)

- Question: "Dimana anda ingin bertemu dengan Tim Prudential?"
- Options:
  1. Di Rumah
  2. Di Kantor
  3. Di Area Publik (Kafe/Mall)

#### Success Screen

- Thank you message
- Summary of selections
- Confirmation text

## 3. Functionality Specification

### Core Features

1. **Step Navigation:** Forward/backward navigation between steps
2. **Selection State:** Visual feedback for selected options (radio behavior - single selection per step)
3. **Progress Tracking:** Visual progress bar updates based on current step
4. **Form Validation:** Require selection before proceeding
5. **Data Collection:** Store all selections in JavaScript object
6. **Summary Display:** Show all collected data on final step

### User Interactions

- Click option → Select and highlight
- Click "Lanjutkan" → Validate and move to next step
- Click "Kembali" → Return to previous step (hidden on step 1)
- Complete all steps → Show success message

### Edge Cases

- Prevent proceeding without selection (show subtle shake animation)
- Handle browser back button gracefully
- Persist state during session

## 4. Steps & Content (Updated)

### Step 1: Kebutuhan (Protection Type)

- Question: "Apa jenis proteksi asuransi yang anda butuhkan saat ini?"
- Options:
  1. Asuransi Kesehatan
  2. Asuransi Jiwa
  3. Asuransi yang dikaitkan dengan investasi (Unit Link)

### Step 2: Anggaran (Budget)

- Question: "Berapa budget bulanan yang anda alokasikan untuk proteksi keluarga?"
- Options:
  1. Kurang dari Rp 500.000
  2. Rp 500.000 - Rp 1.000.000
  3. Rp 1.000.000 - Rp 2.000.000
  4. Rp 2.000.000 - Rp 5.000.000
  5. Lebih dari Rp 5.000.000

### Step 3: Waktu Hari (Day Preference)

- Question: "Kapan waktu yang lebih nyaman untuk anda?"
- Options:
  1. Weekdays (Senin-Jumat)
  2. Weekend (Sabtu-Minggu)

### Step 4: Waktu Jam (Time Slot)

- Question: "Pilih jam operasional yang tersedia?"
- Options:
  1. 09.00 - 11.00 WIB
  2. 11.00 - 13.00 WIB
  3. 13.00 - 15.00 WIB
  4. 15.00 - 17.00 WIB
  5. 17.00 - 19.00 WIB

### Step 5: Lokasi (Meeting Place)

- Question: "Dimana anda ingin bertemu dengan Tim Prudential?"
- Options:
  1. Di Rumah
  2. Di Kantor
  3. Di Area Publik (Kafe/Mall)

### Step 6: Data Diri (Contact Information)

- Question: "Isi data diri Anda untuk melanjutkan"
- Input Fields:
  1. Nama Lengkap (text input)
  2. No. WhatsApp (tel input)
  3. Email (email input)

### Success Screen

- Thank you message
- Summary of selections
- Confirmation text

## 5. Acceptance Criteria

### Visual Checkpoints

- [ ] Progress bar shows correct active segments based on current step (now 6 steps)
- [ ] Selected options have red border and light red background
- [ ] Unselected options have gray border and white background
- [ ] Hover states work on all interactive elements
- [ ] Card is centered and has proper shadow
- [ ] Mobile responsive (looks good on 320px width)
- [ ] Step 6 input fields are properly styled

### Functional Checkpoints

- [ ] Can select only one option per step (steps 1-5)
- [ ] Cannot proceed without selecting an option (steps 1-5)
- [ ] Cannot proceed without filling all fields (step 6)
- [ ] Back button works from step 2 onwards
- [ ] Progress bar updates correctly
- [ ] Final step shows summary of all selections including contact info
- [ ] All transitions are smooth (200ms)
