<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=200&section=header&text=Hello!%20I'm%20Allen&fontSize=50" />
</p>


import streamlit as st

# Page Configuration
st.set_page_config(page_title="Technical Portfolio", page_icon="🌐", layout="wide")

# Custom CSS for the Cyber-Interactive Design
st.markdown("""
    <style>
    /* Background Gradient (Black, Violet, Blue, Red) */
    .stApp {
        background: linear-gradient(135deg, #000000 10%, #1a0033 40%, #001a33 70%, #330000 100%);
        color: #00FF41; /* Matrix Green */
        font-family: 'Verdana', sans-serif;
    }

    /* Interactive "Glass" Capsule */
    .capsule-container {
        background: rgba(255, 255, 255, 0.05);
        backdrop-filter: blur(10px);
        border: 1px solid rgba(0, 255, 65, 0.3);
        border-radius: 20px;
        padding: 40px;
        box-shadow: 0 0 20px rgba(0, 255, 65, 0.1);
        margin: auto;
        max-width: 900px;
    }

    /* Glow Effect for Headers */
    h1, h2, h3 {
        color: #00FF41 !important;
        text-shadow: 0 0 10px #00FF41;
        text-align: center;
    }

    /* Interactive Tag/Button Styling */
    .tech-tag {
        display: inline-block;
        padding: 8px 15px;
        margin: 5px;
        border: 1px solid #00FF41;
        border-radius: 50px;
        background: rgba(0, 255, 65, 0.1);
        transition: 0.3s;
    }
    .tech-tag:hover {
        background: #00FF41;
        color: black;
        box-shadow: 0 0 15px #00FF41;
    }
    </style>
    """, unsafe_allow_html=True)

# Main Container
with st.container():
    st.markdown('<div class="capsule-container">', unsafe_allow_html=True)
    
    # --- HEADER ---
    st.markdown("<h1>🖥️ TECHNICAL PORTFOLIO</h1>", unsafe_allow_html=True)
    st.markdown("<p style='text-align:center;'><b>Certified Computer Systems Servicing Professional</b><br>Specializing in Network Support, Hardware Maintenance, and FTTH Infrastructure.</p>", unsafe_allow_html=True)
    st.divider()

    # --- INTERACTIVE PROGRESS BARS ---
    st.subheader("🎓 Education & Training")
    col1, col2 = st.columns(2)
    
    with col1:
        st.write("**Asian Development Foundation College (ADFC)**")
        st.caption("Outstanding & Best Student Awardee")
        st.progress(100, text="JDVP Technical Competency: 100%")
    
    with col2:
        st.write("**Cisco Networking Academy**")
        st.caption("Active Enrollment")
        st.progress(75, text="Modules 16-31: 75% Complete")

    st.write("") # Spacer

    # --- TECHNICAL EXPERTISE (Interactive Tags) ---
    st.subheader("🛠️ Technical Expertise")
    skills = [
        "Fiber Optic (FTTH) Setup", "RJ45 Termination (T568A/B)", 
        "Cisco Routing", "HTML/CSS Dev", "Hardware Auditing"
    ]
    
    html_tags = "".join([f'<div class="tech-tag">{skill}</div>' for skill in skills])
    st.markdown(f'<div style="text-align:center;">{html_tags}</div>', unsafe_allow_html=True)

    st.write("") # Spacer

    # --- INTERESTS ---
    st.subheader("🚀 Professional Interests")
    with st.expander("Fiber Optic Technology"):
        st.write("Passionate about the future of internet connectivity in the Philippines and fusion splicing.")
    with st.expander("Network Security"):
        st.write("Studying data protection and security protocols within the Cisco Academy framework.")

    # --- CALL TO ACTION ---
    st.write("")
    if st.button("CONTACT FOR TECHNICAL SUPPORT"):
        st.balloons()
        st.success("Redirecting to communication channels...")

    st.markdown('</div>', unsafe_allow_html=True)


