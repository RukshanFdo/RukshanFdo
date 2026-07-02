export default function Home() {
  return (
    <main style={styles.page}>

      {/* HERO */}
      <section style={styles.hero}>
        <h1 style={styles.title}>Mayeul Rukshan Fernando</h1>

        <p style={styles.subtitle}>
          IT Project Manager | Fintech & Banking Technology | Product Delivery Leader | Cybersecurity (In Training)
        </p>

        <p style={styles.location}>
          📍 Dubai Internet City, UAE • ⚡ Immediate Joiner
        </p>

        <div style={styles.links}>
          <a href="mailto:rukshanfernando345@gmail.com">Email</a>
          <a href="https://linkedin.com/in/mayeul-rukshan-fernando" target="_blank">LinkedIn</a>
          <a href="https://github.com/RukshanFdo" target="_blank">GitHub</a>
        </div>
      </section>

      {/* VALUE */}
      <Section title="Executive Summary">
        <p>
          IT Project Manager with ~4 years of experience delivering banking, fintech, and enterprise systems.
          Strong background in software engineering (WSO2) and enterprise delivery in a Tier-1 bank environment.
          Specializing in regulated project delivery, digital transformation, and cross-functional leadership.
        </p>
      </Section>

      {/* CORE EXPERTISE */}
      <Section title="Core Expertise">
        <List items={[
          "IT Project & Product Delivery (Agile / Hybrid / Waterfall)",
          "Banking & Fintech Systems Implementation",
          "Stakeholder & Vendor Management",
          "Regulatory Compliance (PCI DSS, KYC)",
          "Risk Management & Governance",
          "Technical Documentation (BRD / FRD)"
        ]} />
      </Section>

      {/* EXPERIENCE */}
      <Section title="Experience">

        <Job
          role="IT Project Manager — Nations Trust Bank"
          period="2024 – 2026"
          points={[
            "Delivered HSBC portfolio migration support (large-scale banking transition)",
            "Led Google Pay integration (Amex & Mastercard ecosystem)",
            "Coordinated EVKYC digital onboarding transformation",
            "Supported PCI DSS & SIEM security initiatives",
            "Managed governance using Azure DevOps & MS Project"
          ]}
        />

        <Job
          role="IT Project Manager (Contract) — ElysianMemorial"
          period="2023 – 2024"
          points={[
            "Led AI-based platform delivery from concept to production",
            "Managed engineering team (Next.js, Express.js, Azure)",
            "Owned roadmap, sprint planning, and execution",
            "Delivered within scope, timeline, and budget"
          ]}
        />

        <Job
          role="Software Engineering Intern — WSO2"
          period="2022 – 2023"
          points={[
            "Built enterprise developer tooling for VS Code ecosystem",
            "Designed UI/UX flows and system architecture",
            "Improved system stability and debugging workflows",
            "Worked with enterprise-scale integration systems"
          ]}
        />
      </Section>

      {/* EDUCATION */}
      <Section title="Education">
        <p><b>BEng Software Engineering</b> — University of Westminster</p>
        <p><b>IT Diploma (Distinction)</b> — Informatics Institute of Technology (IIT)</p>
      </Section>

      {/* CERTIFICATIONS */}
      <Section title="Certifications">
        <List items={[
          "Google Project Management Certificate",
          "PMI Project Management Fundamentals",
          "WSO2 API Manager Practitioner",
          "HackerRank Problem Solving & Python"
        ]} />
      </Section>

      {/* CURRENT FOCUS */}
      <Section title="Current Focus (Dubai)">
        <p>
          Expanding into Cybersecurity & Networking:
        </p>
        <List items={[
          "CCNA (Cisco Networking)",
          "CCNP (Advanced Networking)",
          "CEH (Ethical Hacking)",
          "CompTIA Security+"
        ]} />
      </Section>

      {/* LEADERSHIP */}
      <Section title="Leadership & Recognition">
        <List items={[
          "Vice President — IEEE Computer Society (IIT)",
          "IEEE Xtreme Ambassador — Sri Lanka Section",
          "Final Year Student Representative — IIT",
          "Finalist — Global TADHack 2021"
        ]} />
      </Section>

      {/* FOOTER */}
      <footer style={styles.footer}>
        <p>Open to opportunities in IT Project Management, Product Ownership & Fintech Technology.</p>
        <p>© {new Date().getFullYear()} Mayeul Rukshan Fernando</p>
      </footer>

    </main>
  );
}

/* ---------------- COMPONENTS ---------------- */

function Section({ title, children }: any) {
  return (
    <section style={styles.section}>
      <h2 style={styles.h2}>{title}</h2>
      <div style={styles.card}>{children}</div>
    </section>
  );
}

function List({ items }: any) {
  return (
    <ul>
      {items.map((item: string, i: number) => (
        <li key={i}>{item}</li>
      ))}
    </ul>
  );
}

function Job({ role, period, points }: any) {
  return (
    <div style={{ marginBottom: 20 }}>
      <h3 style={styles.h3}>{role}</h3>
      <p style={styles.muted}>{period}</p>
      <ul>
        {points.map((p: string, i: number) => (
          <li key={i}>{p}</li>
        ))}
      </ul>
    </div>
  );
}

/* ---------------- STYLES ---------------- */

const styles: any = {
  page: {
    fontFamily: "Arial, sans-serif",
    padding: "40px",
    maxWidth: "1000px",
    margin: "0 auto",
    color: "#111",
    backgroundColor: "#fff"
  },
  hero: {
    marginBottom: 40
  },
  title: {
    fontSize: 42,
    marginBottom: 10
  },
  subtitle: {
    fontSize: 18,
    color: "#444"
  },
  location: {
    marginTop: 10,
    color: "#666"
  },
  links: {
    marginTop: 15,
    display: "flex",
    gap: 15
  },
  section: {
    marginBottom: 40
  },
  h2: {
    fontSize: 22,
    marginBottom: 10
  },
  h3: {
    fontSize: 18,
    marginBottom: 5
  },
  card: {
    padding: 20,
    border: "1px solid #eee",
    borderRadius: 10
  },
  muted: {
    color: "#666"
  },
  footer: {
    marginTop: 60,
    paddingTop: 20,
    borderTop: "1px solid #eee",
    color: "#555",
    textAlign: "center"
  }
};
