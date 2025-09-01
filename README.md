# portfolio-website
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Github, Mail, Phone } from "lucide-react";
import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-800 p-6 md:p-12">
      {/* Header */}
      <header className="text-center mb-12">
        <motion.h1 
          initial={{ opacity: 0, y: -20 }} 
          animate={{ opacity: 1, y: 0 }} 
          transition={{ duration: 0.6 }}
          className="text-4xl font-bold mb-2"
        >
          Jenisha Bhandari
        </motion.h1>
        <p className="text-lg text-gray-600">C++ & Python Web Developer</p>

        <div className="flex justify-center gap-4 mt-4">
          <a href="mailto:jenishabhandari777@gmail.com">
            <Button variant="outline"><Mail className="w-4 h-4 mr-2" /> Email</Button>
          </a>
          <a href="tel:+919036033886">
            <Button variant="outline"><Phone className="w-4 h-4 mr-2" /> Call</Button>
          </a>
          <a href="https://github.com/jenishabhandari" target="_blank">
            <Button variant="outline"><Github className="w-4 h-4 mr-2" /> GitHub</Button>
          </a>
        </div>
      </header>

      {/* About Section */}
      <section className="max-w-4xl mx-auto mb-12">
        <Card className="rounded-2xl shadow-md">
          <CardContent className="p-6">
            <h2 className="text-2xl font-semibold mb-4">About Me</h2>
            <p>
              I am a <strong>C++ and Python developer</strong> with experience in building scalable web apps.
              I primarily work with <strong>Flask</strong> for backend and <strong>React/HTML/CSS/JavaScript</strong> for frontend.
              Currently, I am expanding my expertise in <strong>Django</strong> for large-scale applications.
            </p>
          </CardContent>
        </Card>
      </section>

      {/* Skills Section */}
      <section className="max-w-4xl mx-auto mb-12">
        <h2 className="text-2xl font-semibold mb-4">Skills</h2>
        <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
          {["C", "C++", "Python", "JavaScript", "React", "HTML/CSS", "Flask", "Django (Learning)", "Git/GitHub"].map(skill => (
            <motion.div key={skill} whileHover={{ scale: 1.05 }} className="bg-white p-3 rounded-xl shadow">
              {skill}
            </motion.div>
          ))}
        </div>
      </section>

      {/* Projects Section */}
      <section className="max-w-4xl mx-auto mb-12">
        <h2 className="text-2xl font-semibold mb-6">Projects</h2>
        <div className="grid gap-6 md:grid-cols-2">
          <Card className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold mb-2">Drug Recommendation System</h3>
              <p className="mb-4">
                Web system suggesting medications based on user input & medical data.
                Built with <strong>Flask backend</strong>, <strong>React frontend</strong>, and SQLite database.
                Migrating backend to <strong>Django</strong> for scalability.
              </p>
              <a href="https://github.com/jenishabhandari" target="_blank">
                <Button>View on GitHub</Button>
              </a>
            </CardContent>
          </Card>

          <Card className="rounded-2xl shadow-md">
            <CardContent className="p-6">
              <h3 className="text-xl font-bold mb-2">Dental Hospital Website</h3>
              <p className="mb-4">
                Appointment & patient management system built with <strong>Flask microservices</strong>
                and a clean <strong>HTML/CSS/JS</strong> interface.
              </p>
              <a href="https://github.com/jenishabhandari" target="_blank">
                <Button>View on GitHub</Button>
              </a>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Education & Achievements */}
      <section className="max-w-4xl mx-auto mb-12 grid md:grid-cols-2 gap-6">
        <Card className="rounded-2xl shadow-md">
          <CardContent className="p-6">
            <h2 className="text-2xl font-semibold mb-4">Education</h2>
            <p><strong>BMS College of Engineering</strong></p>
            <p>Information Science Engineering (2021 – 2025)</p>
          </CardContent>
        </Card>

        <Card className="rounded-2xl shadow-md">
          <CardContent className="p-6">
            <h2 className="text-2xl font-semibold mb-4">Achievements</h2>
            <p><strong>COMPEX Scholarship Grant</strong> – Awarded by Govt. of India/Indian Embassy.</p>
          </CardContent>
        </Card>
      </section>

      {/* Courses */}
      <section className="max-w-4xl mx-auto mb-12">
        <h2 className="text-2xl font-semibold mb-4">Courses & Certifications</h2>
        <ul className="list-disc ml-6">
          <li>Python for Data Science – Coursera</li>
          <li>Red Hat Enterprise Linux – Coursera</li>
          <li>UiPath: Build with StudioX, Automation Foundations</li>
          <li>AI Tools & ChatGPT Workshop – be10x</li>
        </ul>
      </section>

      {/* Interests */}
      <section className="max-w-4xl mx-auto mb-12">
        <h2 className="text-2xl font-semibold mb-4">Interests</h2>
        <p>
          Exploring Django for scalable apps, AI-powered automation, and building creative side projects that blend frontend and backend development.
        </p>
      </section>
    </div>
  );
}
