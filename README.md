<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 3840 2160"
     width="3840" height="2160" font-family="Inter, 'Helvetica Neue', Arial, sans-serif">

  <!-- ================= DEFINITIONS ================= -->
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0"   stop-color="#0A1024"/>
      <stop offset="1"   stop-color="#0A1024"/>
    </linearGradient>
    <linearGradient id="coreMetal" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0" stop-color="#1B2440"/>
      <stop offset="1" stop-color="#0E1428"/>
    </linearGradient>
    <linearGradient id="coreRim" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0"   stop-color="#39E6FF" stop-opacity="0.9"/>
      <stop offset="0.5" stop-color="#39E6FF" stop-opacity="0.4"/>
      <stop offset="1"   stop-color="#8A6BFF" stop-opacity="0.7"/>
    </linearGradient>
    <filter id="softGlow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="6" result="b"/>
      <feMerge><feMergeNode in="b"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="microBlur" x="-10%" y="-10%" width="120%" height="120%">
      <feGaussianBlur stdDeviation="2"/>
    </filter>
  </defs>

  <!-- ================= CANVAS ================= -->
  <rect width="3840" height="2160" fill="url(#bg)"/>

  <!-- ================= TITLE BAND ================= -->
  <text x="160" y="180" fill="#F2F6FF" font-size="128" font-weight="700"
        letter-spacing="-2">Zevo 5D AI Core Sandbox</text>
  <text x="160" y="260" fill="#9AA6C4" font-size="44" font-weight="500"
        letter-spacing="0.4">Flat Binary File Deployment · ANSI C89/90 · Pure-Function Wrappers · Pthreads</text>
  <text x="3680" y="260" text-anchor="end" fill="#6E7A99" font-size="18"
        font-weight="400">Conceptual reference scaffold — 32B-parameter Q4_0 layout is specified, not fully populated.</text>

  <!-- ================= CENTER CORE ================= -->
  <g id="core">
    <rect x="1370" y="470" width="1100" height="520" rx="14"
          fill="url(#coreMetal)" stroke="url(#coreRim)" stroke-width="2"
          filter="url(#softGlow)"/>
    <!-- data rails -->
    <line x1="1400" y1="640" x2="2440" y2="640" stroke="#1E8FA6" stroke-width="2"/>
    <line x1="1400" y1="820" x2="2440" y2="820" stroke="#1E8FA6" stroke-width="2"/>
    <!-- core label -->
    <text x="1920" y="740" text-anchor="middle" fill="#F2F6FF"
          font-family="'JetBrains Mono', monospace" font-size="40" font-weight="600"
          letter-spacing="0.5">Zevo-32B-core-v0.1-Q4_0.bin</text>
    <text x="1920" y="790" text-anchor="middle" fill="#9AA6C4"
          font-family="'JetBrains Mono', monospace" font-size="20" font-weight="400">
      magic 0x5A45564F · version 0x00010000 · align 64 B
    </text>
    <!-- amber origin dot -->
    <circle cx="1920" cy="730" r="0" fill="#FFB347"/>
  </g>

  <!-- origin anchor dot below core, connecting to 5D diagram -->
  <circle cx="1920" cy="1000" r="8" fill="#FFB347"/>

  <!-- ================= 5D COORDINATE DIAGRAM ================= -->
  <g id="diagram5d">
    <!-- caption -->
    <text x="1920" y="1090" text-anchor="middle" fill="#39E6FF"
          font-family="'JetBrains Mono', monospace" font-size="42" font-weight="600">
      V = (O, X, Y, Z, R)
    </text>
    <!-- origin -->
    <circle cx="1920" cy="1330" r="9" fill="#FFB347"/>
    <text x="1950" y="1336" fill="#FFB347"
          font-family="'JetBrains Mono', monospace" font-size="26" font-weight="600">
      V₀ = (0, 0, 0, 0, 0)
    </text>
    <!-- O axis (up) -->
    <line x1="1920" y1="1330" x2="1920" y2="1180" stroke="#39E6FF" stroke-width="1.5"/>
    <polygon points="1920,1170 1914,1184 1926,1184" fill="#39E6FF"/>
    <text x="1920" y="1160" text-anchor="middle" fill="#39E6FF"
          font-family="'JetBrains Mono', monospace" font-size="26" font-weight="600">O</text>
    <!-- X axis (right) -->
    <line x1="1920" y1="1330" x2="2120" y2="1330" stroke="#1E8FA6" stroke-width="1.5"/>
    <polygon points="2130,1330 2116,1324 2116,1336" fill="#1E8FA6"/>
    <text x="2145" y="1338" fill="#1E8FA6"
          font-family="'JetBrains Mono', monospace" font-size="26" font-weight="600">X</text>
    <!-- Y axis (down) -->
    <line x1="1920" y1="1330" x2="1920" y2="1480" stroke="#1E8FA6" stroke-width="1.5"/>
    <polygon points="1920,1490 1914,1476 1926,1476" fill="#1E8FA6"/>
    <text x="1920" y="1520" text-anchor="middle" fill="#1E8FA6"
          font-family="'JetBrains Mono', monospace" font-size="26" font-weight="600">Y</text>
    <!-- Z axis (up-right, depth) -->
    <line x1="1920" y1="1330" x2="2090" y2="1210" stroke="#8A6BFF" stroke-width="1.5"/>
    <polygon points="2098,1204 2086,1208 2092,1216" fill="#8A6BFF"/>
    <text x="2108" y="1204" fill="#8A6BFF"
          font-family="'JetBrains Mono', monospace" font-size="26" font-weight="600">Z</text>
    <!-- R axis (up-left, radial) -->
    <line x1="1920" y1="1330" x2="1750" y2="1210" stroke="#8A6BFF" stroke-width="1.5"/>
    <polygon points="1742,1204 1754,1208 1748,1216" fill="#8A6BFF"/>
    <text x="1700" y="1204" fill="#8A6BFF"
          font-family="'JetBrains Mono', monospace" font-size="26" font-weight="600">R</text>
    <!-- sub note -->
    <text x="1920" y="1560" text-anchor="middle" fill="#6E7A99" font-size="18">
      origin invariant · five axes radiating from center
    </text>
  </g>

  <!-- ================= LEFT ARCHITECTURE STACK ================= -->
  <!-- Card A: File Header & Record Layout -->
  <g id="cardA">
    <rect x="160" y="470" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="200" y="520" fill="#F2F6FF" font-size="30" font-weight="600">
      32-Byte-Aligned File Header &amp; Record Layout</text>
    <line x1="200" y1="536" x2="540" y2="536" stroke="#39E6FF" stroke-width="1.5"/>
    <g font-family="'JetBrains Mono', monospace" font-size="19" fill="#9AA6C4">
      <line x1="200" y1="566" x2="220" y2="566" stroke="#39E6FF" stroke-width="1.5"/>
      <text x="232" y="572">0x0000 · Header 64 B</text>
      <line x1="200" y1="596" x2="220" y2="596" stroke="#1E8FA6" stroke-width="1.5"/>
      <text x="232" y="602">0x0040 · Capacity Segments</text>
      <line x1="200" y1="626" x2="220" y2="626" stroke="#1E8FA6" stroke-width="1.5"/>
      <text x="232" y="632">64-B aligned · FSM + Fuzzy Rule Base</text>
      <line x1="200" y1="656" x2="220" y2="656" stroke="#1E8FA6" stroke-width="1.5"/>
      <text x="232" y="662">64-B aligned · Q4_0 Tensor Block</text>
      <line x1="200" y1="686" x2="220" y2="686" stroke="#1E8FA6" stroke-width="1.5"/>
      <text x="232" y="692">64-B aligned · Neural-Mesh Weights</text>
      <line x1="200" y1="716" x2="220" y2="716" stroke="#1E8FA6" stroke-width="1.5"/>
      <text x="232" y="722">64-B aligned · Entropy / Mamdani Scratch</text>
      <line x1="200" y1="746" x2="220" y2="746" stroke="#1E8FA6" stroke-width="1.5"/>
      <text x="232" y="752">64-B aligned · CRUD Journal</text>
    </g>
  </g>

  <!-- Card B: Q4_0 Packed-Weight Blocks -->
  <g id="cardB">
    <rect x="160" y="810" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="200" y="860" fill="#F2F6FF" font-size="30" font-weight="600">
      Q4_0 Packed-Weight Blocks</text>
    <line x1="200" y1="876" x2="500" y2="876" stroke="#39E6FF" stroke-width="1.5"/>
    <!-- orderly block chips -->
    <g>
      <rect x="200" y="910" width="72" height="48" fill="#1E4A5A" stroke="#39E6FF" stroke-width="1.2" opacity="0.85"/>
      <rect x="284" y="910" width="72" height="48" fill="#141A2E" stroke="#24304F" stroke-width="1.2"/>
      <rect x="368" y="910" width="72" height="48" fill="#1E4A5A" stroke="#39E6FF" stroke-width="1.2" opacity="0.85"/>
      <rect x="452" y="910" width="72" height="48" fill="#141A2E" stroke="#24304F" stroke-width="1.2"/>
      <rect x="536" y="910" width="72" height="48" fill="#1E4A5A" stroke="#39E6FF" stroke-width="1.2" opacity="0.85"/>
      <rect x="620" y="910" width="72" height="48" fill="#141A2E" stroke="#24304F" stroke-width="1.2"/>
      <rect x="704" y="910" width="72" height="48" fill="#1E4A5A" stroke="#39E6FF" stroke-width="1.2" opacity="0.85"/>
      <rect x="788" y="910" width="72" height="48" fill="#141A2E" stroke="#24304F" stroke-width="1.2"/>
    </g>
    <text x="200" y="1010" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="19">
      Q4_0 · 32 weights / 20 B · padded to 64-B boundary</text>
    <!-- bracket label d2 block -->
    <line x1="200" y1="1060" x2="860" y2="1060" stroke="#39E6FF" stroke-width="1.2"/>
    <line x1="200" y1="1050" x2="200" y2="1070" stroke="#39E6FF" stroke-width="1.2"/>
    <line x1="860" y1="1050" x2="860" y2="1070" stroke="#39E6FF" stroke-width="1.2"/>
    <text x="530" y="1092" text-anchor="middle" fill="#39E6FF"
          font-family="'JetBrains Mono', monospace" font-size="20" font-weight="600">d₂ block</text>
  </g>

  <!-- Card C: 32-Byte Alignment · AVX-256 Vector Lanes -->
  <g id="cardC">
    <rect x="160" y="1150" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="200" y="1200" fill="#F2F6FF" font-size="30" font-weight="600">
      32-Byte Alignment Boundaries · AVX-256 Lanes</text>
    <line x1="200" y1="1216" x2="620" y2="1216" stroke="#39E6FF" stroke-width="1.5"/>
    <!-- 8 lanes of 32B -->
    <g>
      <rect x="200" y="1250" width="80" height="60" fill="#39E6FF" opacity="0.14"/>
      <rect x="280" y="1250" width="80" height="60" fill="transparent"/>
      <rect x="360" y="1250" width="80" height="60" fill="#39E6FF" opacity="0.14"/>
      <rect x="440" y="1250" width="80" height="60" fill="transparent"/>
      <rect x="520" y="1250" width="80" height="60" fill="#39E6FF" opacity="0.14"/>
      <rect x="600" y="1250" width="80" height="60" fill="transparent"/>
      <rect x="680" y="1250" width="80" height="60" fill="#39E6FF" opacity="0.14"/>
      <rect x="760" y="1250" width="80" height="60" fill="transparent"/>
    </g>
    <!-- 32B ticks -->
    <g stroke="#39E6FF" stroke-width="1.5">
      <line x1="200" y1="1250" x2="200" y2="1310"/>
      <line x1="280" y1="1250" x2="280" y2="1310"/>
      <line x1="360" y1="1250" x2="360" y2="1310"/>
      <line x1="440" y1="1250" x2="440" y2="1310"/>
      <line x1="520" y1="1250" x2="520" y2="1310"/>
      <line x1="600" y1="1250" x2="600" y2="1310"/>
      <line x1="680" y1="1250" x2="680" y2="1310"/>
      <line x1="760" y1="1250" x2="760" y2="1310"/>
      <line x1="840" y1="1250" x2="840" y2="1310"/>
    </g>
    <!-- 32B markers -->
    <g fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="16">
      <text x="240" y="1240" text-anchor="middle">32 B</text>
      <text x="320" y="1240" text-anchor="middle">32 B</text>
      <text x="400" y="1240" text-anchor="middle">32 B</text>
      <text x="480" y="1240" text-anchor="middle">32 B</text>
      <text x="560" y="1240" text-anchor="middle">32 B</text>
      <text x="640" y="1240" text-anchor="middle">32 B</text>
      <text x="720" y="1240" text-anchor="middle">32 B</text>
      <text x="800" y="1240" text-anchor="middle">32 B</text>
    </g>
    <text x="200" y="1390" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="19">
      AVX-256 · 32-byte lanes · vmovaps aligned load/store</text>
  </g>

  <!-- Card D: Pthreads Parallel Workers & Sharding -->
  <g id="cardD">
    <rect x="160" y="1490" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="200" y="1540" fill="#F2F6FF" font-size="30" font-weight="600">
      Pthreads Parallel Workers &amp; Sharding</text>
    <line x1="200" y1="1556" x2="540" y2="1556" stroke="#39E6FF" stroke-width="1.5"/>
    <!-- source node -->
    <circle cx="230" cy="1630" r="14" fill="#39E6FF"/>
    <!-- workers -->
    <circle cx="370" cy="1630" r="18" fill="#141A2E" stroke="#39E6FF" stroke-width="2"/>
    <text x="370" y="1636" text-anchor="middle" fill="#39E6FF" font-family="'JetBrains Mono', monospace" font-size="16">w₀</text>
    <circle cx="470" cy="1630" r="18" fill="#141A2E" stroke="#39E6FF" stroke-width="2"/>
    <text x="470" y="1636" text-anchor="middle" fill="#39E6FF" font-family="'JetBrains Mono', monospace" font-size="16">w₁</text>
    <circle cx="570" cy="1630" r="18" fill="#141A2E" stroke="#FFB347" stroke-width="2.5"/>
    <text x="570" y="1636" text-anchor="middle" fill="#FFB347" font-family="'JetBrains Mono', monospace" font-size="16">w₂</text>
    <circle cx="670" cy="1630" r="18" fill="#141A2E" stroke="#39E6FF" stroke-width="2"/>
    <text x="670" y="1636" text-anchor="middle" fill="#39E6FF" font-family="'JetBrains Mono', monospace" font-size="16">w₃</text>
    <circle cx="770" cy="1630" r="18" fill="#141A2E" stroke="#39E6FF" stroke-width="2"/>
    <text x="770" y="1636" text-anchor="middle" fill="#39E6FF" font-family="'JetBrains Mono', monospace" font-size="16">w₄</text>
    <!-- sink node -->
    <circle cx="870" cy="1630" r="14" fill="#FFB347"/>
    <!-- fan-out -->
    <g stroke="#1E8FA6" stroke-width="1.5">
      <line x1="244" y1="1630" x2="352" y2="1630"/>
      <line x1="244" y1="1628" x2="452" y2="1626"/>
      <line x1="244" y1="1632" x2="552" y2="1630"/>
      <line x1="244" y1="1634" x2="652" y2="1626"/>
      <line x1="244" y1="1636" x2="752" y2="1628"/>
      <line x1="388" y1="1630" x2="856" y2="1630"/>
      <line x1="488" y1="1630" x2="856" y2="1630"/>
      <line x1="588" y1="1630" x2="856" y2="1630"/>
      <line x1="688" y1="1630" x2="856" y2="1630"/>
      <line x1="788" y1="1630" x2="856" y2="1630"/>
    </g>
    <text x="200" y="1710" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="19">
      pthread_mutex_t · pthread_rwlock_t</text>
    <!-- shard labels -->
    <text x="200" y="1758" fill="#39E6FF" font-family="'JetBrains Mono', monospace" font-size="20" font-weight="600">
      d₀ lane · d₁ vec · d₄ shard</text>
  </g>

  <!-- ================= RIGHT ARCHITECTURE STACK ================= -->
  <!-- Card E: FSM Control Path -->
  <g id="cardE">
    <rect x="2960" y="470" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="3000" y="520" fill="#F2F6FF" font-size="30" font-weight="600">
      FSM Control Path · Fuzzy · Shannon · Mamdani</text>
    <line x1="3000" y1="536" x2="3480" y2="536" stroke="#39E6FF" stroke-width="1.5"/>
    <!-- state chain -->
    <g font-family="'JetBrains Mono', monospace" font-size="18">
      <rect x="3000" y="570" width="110" height="44" rx="8" fill="#141A2E" stroke="#39E6FF" stroke-width="1.5"/>
      <text x="3055" y="597" text-anchor="middle" fill="#39E6FF">IDLE</text>
      <line x1="3110" y1="592" x2="3140" y2="592" stroke="#1E8FA6" stroke-width="1.5"/>
      <polygon points="3148,592 3136,588 3136,596" fill="#1E8FA6"/>
      <rect x="3150" y="570" width="110" height="44" rx="8" fill="#141A2E" stroke="#39E6FF" stroke-width="1.5"/>
      <text x="3205" y="597" text-anchor="middle" fill="#39E6FF">LOAD</text>
      <line x1="3260" y1="592" x2="3290" y2="592" stroke="#1E8FA6" stroke-width="1.5"/>
      <polygon points="3298,592 3286,588 3286,596" fill="#1E8FA6"/>
      <rect x="3300" y="570" width="110" height="44" rx="8" fill="#141A2E" stroke="#FFB347" stroke-width="2.5"/>
      <text x="3355" y="597" text-anchor="middle" fill="#FFB347">INFER</text>
      <line x1="3410" y1="592" x2="3440" y2="592" stroke="#1E8FA6" stroke-width="1.5"/>
      <polygon points="3448,592 3436,588 3436,596" fill="#1E8FA6"/>
      <rect x="3450" y="570" width="110" height="44" rx="8" fill="#141A2E" stroke="#39E6FF" stroke-width="1.5"/>
      <text x="3505" y="597" text-anchor="middle" fill="#39E6FF">LEARN</text>
      <line x1="3560" y1="592" x2="3590" y2="592" stroke="#1E8FA6" stroke-width="1.5"/>
      <polygon points="3598,592 3586,588 3586,596" fill="#1E8FA6"/>
      <rect x="3600" y="570" width="60" height="44" rx="8" fill="#141A2E" stroke="#39E6FF" stroke-width="1.5"/>
      <text x="3630" y="597" text-anchor="middle" fill="#39E6FF">SERVE</text>
    </g>
    <!-- named concepts -->
    <g font-family="'JetBrains Mono', monospace" font-size="18" fill="#9AA6C4">
      <text x="3000" y="680">μ · fuzzy triangular membership</text>
      <text x="3000" y="712">H = −Σ p · log p · Shannon entropy</text>
      <text x="3000" y="744">centroid defuzz · Mamdani inference</text>
    </g>
  </g>

  <!-- Card F: Neural-Mesh Network -->
  <g id="cardF">
    <rect x="2960" y="810" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="3000" y="860" fill="#F2F6FF" font-size="30" font-weight="600">
      Neural-Mesh Network · Autonomous Learning</text>
    <line x1="3000" y1="876" x2="3440" y2="876" stroke="#8A6BFF" stroke-width="1.5"/>
    <!-- 3 layer x 5 node mesh -->
    <g>
      <!-- layer1 -->
      <circle cx="3050" cy="930" r="9" fill="#8A6BFF"/>
      <circle cx="3050" cy="970" r="9" fill="#8A6BFF"/>
      <circle cx="3050" cy="1010" r="9" fill="#8A6BFF"/>
      <circle cx="3050" cy="1050" r="9" fill="#8A6BFF"/>
      <circle cx="3050" cy="1090" r="9" fill="#8A6BFF"/>
      <!-- layer2 -->
      <circle cx="3200" cy="930" r="9" fill="#8A6BFF"/>
      <circle cx="3200" cy="970" r="9" fill="#8A6BFF"/>
      <circle cx="3200" cy="1010" r="9" fill="#8A6BFF"/>
      <circle cx="3200" cy="1050" r="9" fill="#8A6BFF"/>
      <circle cx="3200" cy="1090" r="9" fill="#8A6BFF"/>
      <!-- layer3 -->
      <circle cx="3350" cy="930" r="9" fill="#8A6BFF"/>
      <circle cx="3350" cy="970" r="9" fill="#8A6BFF"/>
      <circle cx="3350" cy="1010" r="9" fill="#8A6BFF"/>
      <circle cx="3350" cy="1050" r="9" fill="#8A6BFF"/>
      <circle cx="3350" cy="1090" r="9" fill="#8A6BFF"/>
    </g>
    <!-- edges (dim) -->
    <g stroke="#4B3A8C" stroke-width="1">
      <line x1="3059" y1="930" x2="3191" y2="970"/>
      <line x1="3059" y1="970" x2="3191" y2="1010"/>
      <line x1="3059" y1="1010" x2="3191" y2="930"/>
      <line x1="3059" y1="1010" x2="3191" y2="1050"/>
      <line x1="3059" y1="1050" x2="3191" y2="1090"/>
      <line x1="3059" y1="1090" x2="3191" y2="1010"/>
      <line x1="3209" y1="930" x2="3341" y2="970"/>
      <line x1="3209" y1="970" x2="3341" y2="1010"/>
      <line x1="3209" y1="1010" x2="3341" y2="930"/>
      <line x1="3209" y1="1010" x2="3341" y2="1050"/>
      <line x1="3209" y1="1050" x2="3341" y2="1090"/>
      <line x1="3209" y1="1090" x2="3341" y2="1010"/>
    </g>
    <!-- active path (violet bright) -->
    <g stroke="#8A6BFF" stroke-width="2">
      <line x1="3059" y1="1010" x2="3191" y2="1010"/>
      <line x1="3209" y1="1010" x2="3341" y2="970"/>
      <line x1="3209" y1="1010" x2="3341" y2="1050"/>
    </g>
    <!-- formula caption -->
    <text x="3000" y="1075" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="16">
      auto weights = f(entropy, mamdani, prev_w)</text>
    <!-- V1 layer tag -->
    <text x="3600" y="1092" fill="#8A6BFF" font-family="'JetBrains Mono', monospace" font-size="22" font-weight="600">V₁</text>
  </g>

  <!-- Card G: Secure CRUD Journal -->
  <g id="cardG">
    <rect x="2960" y="1150" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="3000" y="1200" fill="#F2F6FF" font-size="30" font-weight="600">
      Secure CRUD Journal · Integrity Validation</text>
    <line x1="3000" y1="1216" x2="3440" y2="1216" stroke="#39E6FF" stroke-width="1.5"/>
    <!-- ledger rows -->
    <g font-family="'JetBrains Mono', monospace" font-size="20">
      <line x1="3000" y1="1270" x2="3640" y2="1270" stroke="#24304F" stroke-width="1.5"/>
      <text x="3000" y="1264" fill="#39E6FF" font-weight="600">C</text>
      <text x="3560" y="1264" fill="#FFB347" font-size="22">✓</text>
      <line x1="3000" y1="1310" x2="3640" y2="1310" stroke="#24304F" stroke-width="1.5"/>
      <text x="3000" y="1304" fill="#39E6FF" font-weight="600">R</text>
      <text x="3560" y="1304" fill="#9AA6C4">⏚</text>
      <line x1="3000" y1="1350" x2="3640" y2="1350" stroke="#24304F" stroke-width="1.5"/>
      <text x="3000" y="1344" fill="#39E6FF" font-weight="600">U</text>
      <text x="3560" y="1344" fill="#9AA6C4">⏚</text>
      <line x1="3000" y1="1390" x2="3640" y2="1390" stroke="#24304F" stroke-width="1.5"/>
      <text x="3000" y="1384" fill="#39E6FF" font-weight="600">D</text>
      <text x="3560" y="1384" fill="#9AA6C4">⏚</text>
    </g>
    <text x="3000" y="1430" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="19">
      CIA triad · SHA-256 · pthread_rwlock_t</text>
    <!-- L0 layer tag -->
    <text x="3600" y="1430" fill="#39E6FF" font-family="'JetBrains Mono', monospace" font-size="22" font-weight="600">L₀</text>
  </g>

  <!-- Card H: GPU Compute, Rendering, Audio Validation -->
  <g id="cardH">
    <rect x="2960" y="1490" width="720" height="300" rx="12"
          fill="#141A2E" stroke="#24304F" stroke-width="1.5"/>
    <text x="3000" y="1540" fill="#F2F6FF" font-size="30" font-weight="600">
      GPU Compute · Rendering · Audio Validation</text>
    <line x1="3000" y1="1556" x2="3460" y2="1556" stroke="#39E6FF" stroke-width="1.5"/>
    <!-- GPU compute: 3x3 grid -->
    <g transform="translate(3000,1590)">
      <rect x="0" y="0" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="30" y="0" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="60" y="0" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="0" y="30" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="30" y="30" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="60" y="30" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="0" y="60" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="30" y="60" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
      <rect x="60" y="60" width="24" height="24" fill="#39E6FF" opacity="0.8"/>
    </g>
    <!-- Rendering: wireframe viewport -->
    <g transform="translate(3150,1590)" stroke="#39E6FF" stroke-width="2" fill="none">
      <rect x="0" y="0" width="80" height="80"/>
      <line x1="0" y1="0" x2="80" y2="80"/>
      <line x1="80" y1="0" x2="0" y2="80"/>
    </g>
    <!-- Audio: waveform -->
    <g transform="translate(3300,1590)" stroke="#8A6BFF" stroke-width="2" fill="none">
      <polyline points="0,40 10,40 20,20 30,60 40,10 50,70 60,30 70,50 80,40"/>
    </g>
    <!-- labels -->
    <text x="3000" y="1700" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="18">OpenCL</text>
    <text x="3150" y="1700" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="18">OpenGL (SDL2)</text>
    <text x="3300" y="1700" fill="#9AA6C4" font-family="'JetBrains Mono', monospace" font-size="18">OpenAL</text>
    <!-- P3 / S4 / B2 tags -->
    <text x="3520" y="1700" fill="#8A6BFF" font-family="'JetBrains Mono', monospace" font-size="22" font-weight="600">P₃ · S₄</text>
  </g>

  <!-- ================= CONNECTORS ================= -->
  <g stroke-linecap="round">
    <!-- core → card A -->
    <line x1="1370" y1="600" x2="880" y2="600" stroke="#39E6FF" stroke-width="3"/>
    <circle cx="1370" cy="600" r="6" fill="#39E6FF"/>
    <!-- core → card B -->
    <line x1="1370" y1="720" x2="880" y2="850" stroke="#1E8FA6" stroke-width="1.5"/>
    <circle cx="1370" cy="720" r="5" fill="#1E8FA6"/>
    <!-- core → card D -->
    <line x1="1370" y1="940" x2="880" y2="1640" stroke="#1E8FA6" stroke-width="1.5"/>
    <circle cx="1370" cy="940" r="5" fill="#1E8FA6"/>
    <!-- core → card E -->
    <line x1="2470" y1="600" x2="2960" y2="600" stroke="#39E6FF" stroke-width="3"/>
    <circle cx="2470" cy="600" r="6" fill="#39E6FF"/>
    <!-- core → card F -->
    <line x1="2470" y1="720" x2="2960" y2="900" stroke="#8A6BFF" stroke-width="3"/>
    <circle cx="2470" cy="720" r="6" fill="#8A6BFF"/>
    <!-- core → card G -->
    <line x1="2470" y1="900" x2="2960" y2="1280" stroke="#1E8FA6" stroke-width="1.5"/>
    <circle cx="2470" cy="900" r="5" fill="#1E8FA6"/>
    <!-- card D → card H -->
    <line x1="880" y1="1640" x2="1200" y2="1640" stroke="#1E8FA6" stroke-width="1.5"/>
    <line x1="1200" y1="1640" x2="1200" y2="1740" stroke="#1E8FA6" stroke-width="1.5"/>
    <line x1="1200" y1="1740" x2="2960" y2="1740" stroke="#1E8FA6" stroke-width="1.5"/>
    <!-- core → origin anchor -->
    <line x1="1920" y1="990" x2="1920" y2="1020" stroke="#FFB347" stroke-width="2"/>
    <circle cx="1920" cy="990" r="5" fill="#FFB347"/>
    <!-- card E ↔ card F -->
    <line x1="3320" y1="770" x2="3320" y2="810" stroke="#8A6BFF" stroke-width="1.5"/>
    <polygon points="3320,820 3316,808 3324,808" fill="#8A6BFF"/>
    <polygon points="3320,760 3316,772 3324,772" fill="#8A6BFF"/>
  </g>

  <!-- ================= FOOTER ================= -->
  <line x1="160" y1="2000" x2="3680" y2="2000" stroke="#24304F" stroke-width="1.5"/>

  <!-- Capacity labels -->
  <g font-family="'JetBrains Mono', monospace" font-size="22" fill="#39E6FF" font-weight="600">
    <text x="160"  y="2070">d₀ lane</text>
    <text x="360"  y="2070">d₁ vec</text>
    <text x="560"  y="2070">d₂ block</text>
    <text x="780"  y="2070">d₄ shard</text>
  </g>

  <!-- Layer labels -->
  <g font-family="'JetBrains Mono', monospace" font-size="22" fill="#8A6BFF" font-weight="600">
    <text x="2800" y="2070">L₀</text>
    <text x="2940" y="2070">V₁</text>
    <text x="3080" y="2070">B₂</text>
    <text x="3220" y="2070">P₃</text>
    <text x="3360" y="2070">S₄</text>
  </g>

  <!-- footer micro-credit -->
  <text x="3680" y="2070" text-anchor="end" fill="#6E7A99" font-size="16">
    Zevo 5D AI Core · v0.1
  </text>

  <!-- tiny footnote: exact readouts -->
  <text x="1920" y="1990" text-anchor="middle" fill="#6E7A99" font-family="'JetBrains Mono', monospace" font-size="16">
    V = (O, X, Y, Z, R)   ·   V₀ = (0, 0, 0, 0, 0)
  </text>

</svg>

---

<img width="832" height="448" alt="Image" src="https://github.com/user-attachments/assets/75882524-95f0-42bb-9f28-8c7d6533f2ec" />

---

## ZEVO — 5D AI-DRIVEN MULTIMODAL SOFTWARE FRAMEWORK™

### Software Architecture Specification

**Document ID:** ZEVO-ARCH-SPEC-001
**Revision:** 1.0
**Classification:** Technical Specification
**Language Standard:** ANSI C89/C90 (ISO/IEC 9899:1990)
**Target ABI:** x86_64 System V ELF ET_DYN

---

## 1. Scope and Purpose

This specification defines the modular software architecture of the Zevo 5D AI-Driven Multimodal Software Framework. Zevo is presented as a layered, C89/C90-compatible runtime for constructing the Native Zevo AI-Driven Core and its associated responsive web application development surface. The framework provides pure-function wrappers in ANSI C89/C90 over supported external libraries.

The architecture is organized into five numbered horizontal layers. Each layer depends only on the stable interfaces published by the layer beneath it. Replaceable components are isolated behind opaque handles and versioned vtables. Platform-specific code is confined to designated modules and does not leak into portable code.

---

## 2. Layered Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         ZEVO 5D FRAMEWORK — LAYER STACK                     │
└─────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────┐
│ LAYER 1 — APPLICATION & CLIENT INTERFACES                                   │
│                                                                             │
│   ┌──────────────┐   ┌──────────────┐   ┌──────────────────────────┐        │
│   │ CLI Client   │   │ GUI Client   │   │ Embedded / Service Host  │        │
│   └──────┬───────┘   └──────┬───────┘   └────────────┬─────────────┘        │
│          │                  │                        │                      │
│          └──────────────────┼────────────────────────┘                      │
│                             ▼                                               │
│              ┌──────────────────────────────────────┐                       │
│              │   IPC / API REQUEST–RESPONSE         │                       │
│              │   Versioned messages · Sync / async  │                       │
│              │   · Streaming                        │                       │
│              └──────────────────┬───────────────────┘                       │
└─────────────────────────────────┼───────────────────────────────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│ LAYER 2 — SERVICES & ORCHESTRATION                                          │
│                                                                             │
│   ┌────────────────────┐ ┌────────────────────┐ ┌────────────────────────┐  │
│   │ Session / Context  │ │ Decision Policy    │ │ Task / Pipeline        │  │
│   │ Service            │ │ Engine             │ │ Orchestrator           │  │
│   └────────────────────┘ └────────────────────┘ └────────────────────────┘  │
│                                                                             │
│   ┌──────────────────────────────────────┐ ┌──────────────────────────────┐ │
│   │ Dependency Interfaces                │ │ Versioned Configuration      │ │
│   │ (vtable / callback)                  │ │ (schema + compatibility      │ │
│   │                                      │ │  rules)                      │ │
│   └──────────────────────────────────────┘ └──────────────────────────────┘ │
└─────────────────────────────────┬───────────────────────────────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│ LAYER 3 — MODALITY ADAPTERS & REPLACEABLE MODEL RUNTIMES                    │
│                                                                             │
│   ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────────────────────────┐          │
│   │ Text │ │Audio │ │Image │ │Video │ │     I/O Devices          │          │
│   └──┬───┘ └──┬───┘ └──┬───┘ └──┬───┘ └────────────┬─────────────┘          │
│      │        │        │        │                  │                        │
│      └────────┴────────┴────────┴──────────────────┘                        │
│                             │                                               │
│              ┌──────────────┴──────────────┐                                │
│              ▼                             ▼                                │
│   ┌────────────────────────┐   ┌────────────────────────┐                   │
│   │ Runtime A (e.g., Zevo) │   │ Runtime B (e.g.,custom)│                   │
│   └────────────────────────┘   └────────────────────────┘                   │
│                    ◄── Replaceable ──►                                      │
└─────────────────────────────────┬───────────────────────────────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│ LAYER 4 — REUSABLE C89/C90 LIBRARIES & APIs                                 │
│                                                                             │
│   ┌────────────────────┐ ┌────────────────────┐ ┌────────────────────┐      │
│   │ Memory Management  │ │ String / Buffer    │ │ Math / Vector      │      │
│   └────────────────────┘ └────────────────────┘ └────────────────────┘      │
│   ┌────────────────────┐ ┌────────────────────┐ ┌────────────────────┐      │
│   │ Logging / Trace    │ │ Config Parser      │ │ IPC / Message Codec│      │
│   └────────────────────┘ └────────────────────┘ └────────────────────┘      │
│   ┌────────────────────┐ ┌────────────────────┐                             │
│   │ Error Handling     │ │Platform Abstraction│                             │
│   └────────────────────┘ └────────────────────┘                             │
│                                                                             │
│   Stable headers · Opaque handles · No implementation leakage               │
└─────────────────────────────────┬───────────────────────────────────────────┘
                                  ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│ LAYER 5 — NATIVE ELF DEPLOYMENT & RUNTIME FOUNDATION                        │
│                                                                             │
│   ┌─────────────────────────────────────────────────────────────────────┐   │
│   │  ELF Image Binary — complete access to LLM-workload Loader          │   │
│   │  (static or dynamic)                                                │   │
│   └─────────────────────────────────────────────────────────────────────┘   │
│   ┌─────────────────────────────────────────────────────────────────────┐   │
│   │  Core Service (model loading, scheduling)                           │   │
│   └─────────────────────────────────────────────────────────────────────┘   │
│   ┌─────────────────────────────────────────────────────────────────────┐   │
│   │  Syscall / Sysenter access hardware device using Assembly Inline    │   │
│   │  on ANSI C89/90                                                     │   │
│   └─────────────────────────────────────────────────────────────────────┘   │
│                                                                             │
│   GNU inline assembly isolated behind platform-specific modules.            │
│   Native binary deployment · No VM required · OS-level integration          │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Figure 1.** Five-layer Zevo framework stack with downward dependency arrows.

---

## 3. Design Principles

| # | Principle | Description |
|---|-----------|-------------|
| 1 | **Opaque handles + stable headers** | All public APIs expose incomplete types. Implementation details remain private. |
| 2 | **Replaceable dependency interfaces** | Runtime and modality backends bind through vtables and callbacks. |
| 3 | **Versioned configuration** | Schema evolution follows explicit compatibility rules. |
| 4 | **Platform-specific code isolated** | Inline assembly and syscall paths are confined to dedicated modules. |

> **Note:** ANSI C89/C90 is a language standard, not an architecture.

---

## 4. Zevo™ System Overview

**Zevo™** — An 5D artificial intelligence virtual assistant.

Zevo is an original, friendly 3D animated AI avatar with expressive features and premium family-film-quality character design. The system presents a clear left-to-right flow:

```
┌──────────────────────┐    ┌──────────────────┐    ┌──────────────────────┐
│ Responsive,          │───►│ Published        │───►│ Secure Autonomous    │
│ Accessible Web       │    │ IPC API          │    │ Zevo AI Core         │
│ Client               │    │                  │    │                      │
│ (stateless, no       │    │                  │    │                      │
│  model weights)      │    │                  │    │                      │
└──────────────────────┘    └──────────────────┘    └───────────┬──────────┘
           ▲                                                    │
           │            Multimodal results returned             │
           └────────────────────────────────────────────────────┘
```

**Figure 2.** Left-to-right request flow. The client holds no model weights.

### 4.1 Input and Output Modalities

| Modality | Representation |
|----------|----------------|
| Raw text | UTF-8 byte stream |
| Images   | BGRA |
| Video    | BGRA |
| Audio    | PCM  |
| I/O      | Devices Peripheral |

These five modalities fuse into a five-dimensional spherical representation:

- **O** — Origin
- **X** — Horizontal
- **Y** — Vertical
- **Z** — Depth
- **R** — Radial Base

The 5D representation is modeled as a spherical coordinate graphic, not as an abstract vector.

---

## 5. AI Core Engine

The ELF Image Binary functions as the AI Core Engine supporting complete LLM workload. Supported model images include:

- `Zevo-64B-Chatbot-Instruct-v0.1-Q8_0.bin`
- `Zevo-32B-Chatbot-Instruct-v0.1-Q4_0.bin`

Model image format: **x86_64 System V ELF ET_DYN**.

### 5.1 Internal ELF Section Schematic

```
┌─────────────────────────────────────────────────────────────┐
│  ELF ET_DYN IMAGE                                           │
│                                                             │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Metadata                                              │  │
│  │   · 32/64-bit alignment                               │  │
│  │   · page-aligned read-only mmap                       │  │
│  │   · ext4 storage                                      │  │
│  │   · fs-verity integrity protection                    │  │
│  └───────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Vectors                                               │  │
│  │   · 32/64-bit alignment                               │  │
│  │   · page-aligned read-only mmap                       │  │
│  └───────────────────────────────────────────────────────┘  │
│  ┌───────────────────────────────────────────────────────┐  │
│  │ Weights                                               │  │
│  │   · 32/64-bit alignment                               │  │
│  │   · page-aligned read-only mmap                       │  │
│  └───────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
```

**Figure 3.** ELF internal sections with alignment, mmap, storage, and integrity properties.

### 5.2 Multimodal Processing Pipeline

A deterministic multimodal processing pipeline feeds an autonomous decision engine. The decision engine combines:

- FSM rules and facts
- Fuzzy-neural mesh
- Shannon entropy
- Mamdani inference
- Machine Learning

These components perform real-time weight calculation and learning. The core communicates outward only through the published IPC API.

---

## 6. Security Architecture

Security is organized as a layered, understandable system.

```
┌─────────────────────────────────────────────────────────────┐
│  SECURE SERVICE API                                         │
│  Mediates cryptographic access                              │
│                                                             │
│  · API keys rotate every 28 hours                           │
│  · OpenSSL primitives aligned with:                         │
│      – NIST SP 800-38D                                      │
│      – NIST SP 800-107                                      │
│      – FIPS 186-5                                           │
├─────────────────────────────────────────────────────────────┤
│  HARDWARE ACCESS                                            │
│  Only through libc wrappers to x86_64 syscall interfaces    │
│  Legacy x86 sysenter noted as a compatibility path          │
│                                                             │
│  · seccomp-BPF                                              │
│  · capability bounding                                      │
│  · LSM controls                                             │
├─────────────────────────────────────────────────────────────┤
│  LANGUAGE & ABI BOUNDARY                                    │
│  · Pure-function wrappers in ANSI C89/C90 with inline       │
│    assembly                                                 │
│  · System V x86_64 and GNU/POSIX compatibility              │
│  · Security-compliance boundaries                           │
└─────────────────────────────────────────────────────────────┘
```

**Figure 4.** Layered security and hardware-access model.

> **Clarification:** These are architecture and interface concepts. They are not claims that model weights themselves implement cryptography or system security.

---

## 7. Deployment Summary

| Property | Value |
|----------|-------|
| Language standard | ANSI C89/C90 |
| ABI | x86_64 System V |
| Binary format | ELF ET_DYN |
| Model loader | Static or dynamic |
| VM requirement | None |
| OS integration | Native, syscall-level |
| Integrity | fs-verity |
| Storage | ext4 |

---

## 8. Diagram — Full System Flow

```
┌──────────────┐   ┌──────────────┐   ┌──────────────┐
│ CLI Client   │   │ GUI Client   │   │ Embedded /   │
│              │   │              │   │ Service Host │
└──────┬───────┘   └──────┬───────┘   └──────┬───────┘
       │                  │                  │
       └──────────────────┼──────────────────┘
                          ▼
              ┌────────────────────────┐
              │ IPC / API Request–     │
              │ Response               │
              └───────────┬────────────┘
                          ▼
       ┌──────────────────┼──────────────────┐
       ▼                  ▼                  ▼
┌─────────────┐  ┌─────────────┐  ┌──────────────────┐
│ Session /   │  │ Decision    │  │ Task / Pipeline  │
│ Context     │  │ Policy      │  │ Orchestrator     │
│ Service     │  │ Engine      │  │                  │
└─────────────┘  └─────────────┘  └──────────────────┘
       │                  │                  │
       └──────────────────┼──────────────────┘
                          ▼
       ┌──────────────────┼──────────────────┐
       ▼                  ▼                  ▼
┌─────────────┐  ┌─────────────┐  ┌──────────────────┐
│ Text        │  │ Audio       │  │ Image / Video /  │
│ Adapter     │  │ Adapter     │  │ I/O Devices      │
└──────┬──────┘  └──────┬──────┘  └────────┬─────────┘
       │                │                  │
       └────────────────┼──────────────────┘
                        ▼
          ┌─────────────┴─────────────┐
          ▼                           ▼
┌──────────────────┐        ┌──────────────────┐
│ Runtime A        │        │ Runtime B        │
│ (e.g., Zevo)     │        │ (e.g., custom)   │
└────────┬─────────┘        └────────┬─────────┘
         └─────────────┬─────────────┘
                       ▼
       ┌───────────────────────────────────┐
       │ Reusable C89/C90 Libraries & APIs │
       │ Memory · String · Math · Logging  │
       │ Config · IPC Codec · Error · PAL  │
       └───────────────┬───────────────────┘
                       ▼
       ┌───────────────────────────────────┐
       │ Native ELF Deployment & Runtime   │
       │ Foundation                        │
       │ ELF Loader · Core Service ·       │
       │ Syscall / Sysenter (inline asm)   │
       └───────────────────────────────────┘
```

**Figure 5.** End-to-end request flow from clients to native runtime foundation.

---

## 9. Design Principles Callout

```
┌─────────────────────────────────────────────┐
│           DESIGN PRINCIPLES                 │
│                                             │
│  1. Opaque handles + stable headers         │
│  2. Replaceable dependency interfaces       │
│  3. Versioned configuration                 │
│  4. Platform-specific code isolated         │
│                                             │
│  Note: ANSI C89/C90 is a language           │
│  standard, not an architecture.             │
└─────────────────────────────────────────────┘
```

---

## 10. Compliance and Boundary Statement

- Pure-function wrappers are provided in ANSI C89/C90 with inline assembly where required.
- System V x86_64 and GNU/POSIX compatibility are maintained at the interface boundary.
- Security-compliance boundaries are enforced at the Secure Service API.
- Model weights, vectors, and metadata are data artifacts. They do not themselves implement cryptographic or system-security functions.

---

*End of Specification — ZEVO-ARCH-SPEC-001 Rev. 1.0*
