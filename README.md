
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>E‑commerce Products Table + Customer Registration</title>
  <style>
    :root{--bg:#f4f7fb;--card:#ffffff;--accent:#0b78d1;--muted:#6b7280;--glass:rgba(255,255,255,0.6)}
    *{box-sizing:border-box}
    body{font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; margin:24px; background:linear-gradient(180deg,var(--bg),#eef3fb); color:#111}
    h1{font-size:1.4rem;margin:0 0 12px}
    .container{max-width:1100px;margin:0 auto}

    /* Card */
    .card{background:var(--card);border-radius:12px;padding:18px;box-shadow:0 6px 20px rgba(16,24,40,0.08);}

    /* Table styles */
    table{width:100%;border-collapse:collapse;font-size:0.95rem}
    thead th{background:linear-gradient(90deg,rgba(11,120,209,0.08),rgba(11,120,209,0.03));padding:12px 10px;text-align:left;border-bottom:1px solid #e6eef8;color:var(--accent)}
    tbody td{padding:12px 10px;border-bottom:1px dashed #eef4fb;vertical-align:top}
    tbody tr:hover{background:linear-gradient(90deg,rgba(11,120,209,0.02),transparent)}

    /* Firm column (icon + name) */
    .firm{display:flex;align-items:center;gap:10px}
    .logo{width:46px;height:46px;border-radius:10px;display:inline-grid;place-items:center;font-weight:700;color:white}
    .logo svg{width:28px;height:28px}
    .firm-name{font-weight:600}
    .muted{color:var(--muted);font-size:0.9rem}

    /* Category badge */
    .badge{display:inline-block;padding:6px 8px;border-radius:999px;font-size:0.78rem;background:#f1f6ff;color:var(--accent);border:1px solid rgba(11,120,209,0.08)}

    /* Product description list inside table cell */
    .desc ul{margin:6px 0 0;padding-left:18px}

    /* Registration form */
    .grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
    label{display:block;font-size:0.85rem;margin-bottom:6px}
    input[type=text], input[type=email], input[type=password], select{width:100%;padding:10px;border-radius:8px;border:1px solid #d7e3f5;background:var(--glass)}
    .full{grid-column:1 / -1}
    .actions{display:flex;gap:12px;align-items:center;margin-top:8px}
    button{background:var(--accent);color:white;padding:10px 14px;border-radius:10px;border:none;cursor:pointer}
    button.secondary{background:transparent;border:1px solid #cce3fb;color:var(--accent)}
    .hint{font-size:0.85rem;color:var(--muted)}

    /* Responsive */
    @media (max-width:800px){.grid{grid-template-columns:1fr}.logo{width:40px;height:40px}
      thead th{font-size:0.85rem} tbody td{font-size:0.92rem}}
  </style>
</head>
<body>
  <div class="container">
    <h1>E‑commerce products table (min. 15 items) + customer registration form</h1>

    <section class="card" aria-labelledby="products-heading">
      <h2 id="products-heading" style="font-size:1.1rem;margin-bottom:10px">Products</h2>
      <div style="overflow:auto">
        <table role="table" aria-label="E-commerce products">
          <thead>
            <tr>
              <th>e‑commerce firm</th>
              <th>product name</th>
              <th>category</th>
              <th>product description</th>
            </tr>
          </thead>
          <tbody>
            <!-- 1 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#ff6b6b">AF
                  </div>
                  <div>
                    <div class="firm-name">AfriMart</div>
                    <div class="muted">www.afrimart.com</div>
                  </div>
                </div>
              </td>
              <td>Solar Lantern X100</td>
              <td><span class="badge">Home & Living</span></td>
              <td class="desc">
                <ul>
                  <li>Rechargeable LED lantern (8–48 hrs)</li>
                  <li>USB charging + solar panel</li>
                  <li>Durable, splash resistant</li>
                </ul>
              </td>
            </tr>

            <!-- 2 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#0b78d1">BK
                  </div>
                  <div>
                    <div class="firm-name">BuyKwani</div>
                    <div class="muted">marketplace</div>
                  </div>
                </div>
              </td>
              <td>Artisan Shea Butter (250g)</td>
              <td><span class="badge">Beauty</span></td>
              <td class="desc"><ul>
                <li>Cold-pressed, unrefined</li>
                <li>Nutritive for skin & hair</li>
                <li>Locally sourced</li>
              </ul></td>
            </tr>

            <!-- 3 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#34c759">ZT</div>
                  <div>
                    <div class="firm-name">ZetuTech</div>
                    <div class="muted">electronics</div>
                  </div>
                </div>
              </td>
              <td>Bluetooth Earbuds A2</td>
              <td><span class="badge">Electronics</span></td>
              <td class="desc"><ul>
                <li>Noise reduction, 24h battery</li>
                <li>Water-resistant IPX5</li>
                <li>Bluetooth 5.2</li>
              </ul></td>
            </tr>

            <!-- 4 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#ffb020">MB</div>
                  <div>
                    <div class="firm-name">Mbogi</div>
                    <div class="muted">fashion</div>
                  </div>
                </div>
              </td>
              <td>Canvas School Backpack</td>
              <td><span class="badge">Accessories</span></td>
              <td class="desc"><ul>
                <li>Durable cotton canvas</li>
                <li>Padded straps & laptop sleeve</li>
                <li>Multiple compartments</li>
              </ul></td>
            </tr>

            <!-- 5 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#7f5af0">TK</div>
                  <div>
                    <div class="firm-name">TokaKart</div>
                    <div class="muted">fresh goods</div>
                  </div>
                </div>
              </td>
              <td>Organic Avocado (kg)</td>
              <td><span class="badge">Groceries</span></td>
              <td class="desc"><ul>
                <li>Locally grown, ripe</li>
                <li>No pesticides</li>
                <li>Delivered same-day</li>
              </ul></td>
            </tr>

            <!-- 6 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#ff7ab6">GR</div>
                  <div>
                    <div class="firm-name">Griya</div>
                    <div class="muted">home</div>
                  </div>
                </div>
              </td>
              <td>Handwoven Basket (medium)</td>
              <td><span class="badge">Home</span></td>
              <td class="desc"><ul>
                <li>Natural sisal & cotton</li>
                <li>Perfect for storage</li>
                <li>Handmade — each unique</li>
              </ul></td>
            </tr>

            <!-- 7 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#00a3ff">ND</div>
                  <div>
                    <div class="firm-name">NdiMarket</div>
                    <div class="muted">electronics</div>
                  </div>
                </div>
              </td>
              <td>Smartwatch S3</td>
              <td><span class="badge">Wearables</span></td>
              <td class="desc"><ul>
                <li>Heart rate + sleep tracking</li>
                <li>Waterproof 50m</li>
                <li>7-day battery life</li>
              </ul></td>
            </tr>

            <!-- 8 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#ff9f1c">KM</div>
                  <div>
                    <div class="firm-name">KijijiMall</div>
                    <div class="muted">books & paper</div>
                  </div>
                </div>
              </td>
              <td>Primary School Maths Textbook</td>
              <td><span class="badge">Books</span></td>
              <td class="desc"><ul>
                <li>Aligned to national syllabus</li>
                <li>Clear diagrams and exercises</li>
                <li>Includes answer key</li>
              </ul></td>
            </tr>

            <!-- 9 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#6ee7b7">SR</div>
                  <div>
                    <div class="firm-name">SokoRural</div>
                    <div class="muted">agri</div>
                  </div>
                </div>
              </td>
              <td>Fertilizer NPK 10-20-10 (25kg)</td>
              <td><span class="badge">Agriculture</span></td>
              <td class="desc"><ul>
                <li>Balanced nutrients for cereals</li>
                <li>Bulk & retail packaging</li>
                <li>Application instructions included</li>
              </ul></td>
            </tr>

            <!-- 10 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#8b5cf6">PL</div>
                  <div>
                    <div class="firm-name">PulseLab</div>
                    <div class="muted">health</div>
                  </div>
                </div>
              </td>
              <td>Digital Blood Pressure Monitor</td>
              <td><span class="badge">Health</span></td>
              <td class="desc"><ul>
                <li>Large display, memory for 2 users</li>
                <li>Clinically validated</li>
                <li>Includes cuff & batteries</li>
              </ul></td>
            </tr>

            <!-- 11 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#ff4d6d">BB</div>
                  <div>
                    <div class="firm-name">BoraBora</div>
                    <div class="muted">toys</div>
                  </div>
                </div>
              </td>
              <td>Educational Wooden Puzzle</td>
              <td><span class="badge">Toys</span></td>
              <td class="desc"><ul>
                <li>Age 3+, safe paint</li>
                <li>Improves hand-eye coordination</li>
                <li>Eco-friendly wood</li>
              </ul></td>
            </tr>

            <!-- 12 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#00c2a8">CL</div>
                  <div>
                    <div class="firm-name">CityLines</div>
                    <div class="muted">sports</div>
                  </div>
                </div>
              </td>
              <td>Running Shoes — Model R</td>
              <td><span class="badge">Sports</span></td>
              <td class="desc"><ul>
                <li>Lightweight foam midsole</li>
                <li>Breathable mesh upper</li>
                <li>Available sizes 36–46</li>
              </ul></td>
            </tr>

            <!-- 13 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#ff5a00">FM</div>
                  <div>
                    <div class="firm-name">FarmLink</div>
                    <div class="muted">produce</div>
                  </div>
                </div>
              </td>
              <td>Fresh Eggs (tray 30)</td>
              <td><span class="badge">Groceries</span></td>
              <td class="desc"><ul>
                <li>Grade A, free-range</li>
                <li>Clean packing and delivery</li>
                <li>Price per tray</li>
              </ul></td>
            </tr>

            <!-- 14 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#9b8cfc">ED</div>
                  <div>
                    <div class="firm-name">EduBox</div>
                    <div class="muted">learning</div>
                  </div>
                </div>
              </td>
              <td>Junior Coding Kit</td>
              <td><span class="badge">Education</span></td>
              <td class="desc"><ul>
                <li>Block-based lessons (ages 8+)</li>
                <li>Simple electronics & guidebook</li>
                <li>Includes project stickers</li>
              </ul></td>
            </tr>

            <!-- 15 -->
            <tr>
              <td>
                <div class="firm">
                  <div class="logo" style="background:#2b7a78">RP</div>
                  <div>
                    <div class="firm-name">RoboPlus</div>
                    <div class="muted">gadgets</div>
                  </div>
                </div>
              </td>
              <td>Mini Robotic Car Kit</td>
              <td><span class="badge">Hobby</span></td>
              <td class="desc"><ul>
                <li>Includes chassis, motors, sensors</li>
                <li>Works with Arduino and blocks</li>
                <li>Beginner-friendly projects</li>
              </ul></td>
            </tr>

          </tbody>
        </table>
      </div>
    </section>

    <section style="height:18px"></section>

    <section class="card" aria-labelledby="register-heading" style="margin-top:14px">
      <h2 id="register-heading" style="font-size:1.1rem;margin-bottom:10px">Customer registration form</h2>
      <form id="regForm" onsubmit="return handleSubmit(event)" novalidate>
        <div class="grid">
          <div>
            <label for="fname">First name</label>
            <input id="fname" name="fname" type="text" required placeholder="Debra" />
          </div>

          <div>
            <label for="lname">Last name</label>
            <input id="lname" name="lname" type="text" required placeholder="Flora" />
          </div>

          <div>
            <label for="email">Email address</label>
            <input id="email" name="email" type="email" required placeholder="name@gmail.com" />
          </div>

          <div>
            <label for="phone">Phone number</label>
            <input id="phone" name="phone" type="text" pattern="^\\+?[0-9\s-]{7,20}$" placeholder="+254 7xx xxx xxx" />
          </div>

          <div>
            <label for="password">Password</label>
            <input id="password" name="password" type="password" minlength="8" required placeholder="At least 8 characters" />
          </div>

          <div>
            <label for="confirm">Confirm password</label>
            <input id="confirm" name="confirm" type="password" required placeholder="Repeat password" />
          </div>

          <div class="full">
            <label for="address">Address</label>
            <input id="address" name="address" type="text" placeholder="City" />
          </div>

          <div>
            <label for="gender">Gender</label>
            <select id="gender" name="gender">
              <option value="">Female</option>
              <option value="female">Female</option>
              <option value="male">Male</option>
              <option value="other">Other</option>
            </select>
          </div>

          <div>
            <label for="dob">Date of birth</label>
            <input id="dob" name="dob" type="text" placeholder="YYYY-MM-DD" />
          </div>

          <div class="full">
            <label>Preferences</label>
            <div style="display:flex;gap:8px;flex-wrap:wrap">
              <label style="font-weight:600"><input type="checkbox" name="pref" value="offers"> Email offers</label>
              <label style="font-weight:600"><input type="checkbox" name="pref" value="sms"> SMS alerts</label>
              <label style="font-weight:600"><input type="checkbox" name="pref" value="newsletter"> Newsletter</label>
            </div>
          </div>

        </div>

        <div class="actions">
          <button type="submit">Create account</button>
          <button type="button" class="secondary" onclick="document.getElementById('regForm').reset()">Reset</button>
          <div class="hint">By creating an account you agree to our <a href="#">terms</a>.</div>
        </div>
      </form>
    </section>

  </div>

  <script>
    function showError(el, msg){
      el.setCustomValidity(msg || '');
    }

    function clearError(el){ el.setCustomValidity(''); }

    function handleSubmit(e){
      e.preventDefault();
      const form = e.target;
      const pw = form.password.value;
      const conf = form.confirm.value;
      clearError(form.password);
      clearError(form.confirm);
      if(pw.length < 8){ showError(form.password,'Password must be at least 8 characters'); form.password.reportValidity(); return false }
      if(pw !== conf){ showError(form.confirm,'Passwords do not match'); form.confirm.reportValidity(); return false }

      // Minimal front-end email format check handled by input[type=email]

      // If all good — show a simple success message (replace with real signup call)
      alert('Account created (demo).\nDetails:\nName: '+form.fname.value+' '+form.lname.value+'\nEmail: '+form.email.value);
      form.reset();
      return false;
    }
  </script>
</body>
</html>
