# Release notes
- Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Observation-Histologie 
- Attribut: Observation.effective (Histologie-Datum)
	- Änderung: hinzugefügt
- Attribut: Observation.value.text (Morphologie-Freitext)
	- Änderung: hinzugefügt
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Observation-GenetischeVariante
  - Änderung: hinzugefügt, um die laufenden Umfragen zu den molekularen Markern an den DKTK-Standorten abzudecken  
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Procedure-Operation
- Attribut: Procedure.performed (OP-Datum) 
	- Änderung: hinzugefügt: OP-Datum hinzugefügt und als must-support festgelegt
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Condition-Primaerdiagnose
- Attribut: Condition.code.coding 
	- Änderung: hinzugefügt: weitere Kodierungssysteme wurden für die Kompatibilität mit BBMRI hinzugefügt
		- Varianten: Alpha-ID, SNOMED CT, Orphanet   
- Attribut: Condition.code.text 
	- Änderung: hinzugefügt: Primaertumor-Diagnosetext

- Attribut: Condition.bodySite.coding:ADT-Seitenlokalisation.system
	- Änderung: ersetzt: "urn:oid:2.16.840.1.113883.2.6.60.7.1.1" durch "http://dktk.dkfz.de/fhir/onco/core/CodeSystem/SeitenlokalisationCS ersetzt 

- Attribut: Condition.bodySite.coding
	- Änderung: hinzugefügt: SNOMED CT für die Kompatibilität mit BBMRI hinzugefügt
- Attribut: Condition.onset:onsetAge
	- Änderung: gelöscht: onsetAge (Alter bei Erstdiagnose) gelöscht, da es mit dem Diagnosedatum nicht kombinierbar ist. Das Feld kann trotzdem indirekt berechnet werden
- Attribut: Condition.evidence.detail
	- Änderung: referenziert: Integration von http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Observation-TodUrsache in das Condition-Profil 	
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Procedure-Strahlentherapie
- Attribut: Procedure.performed.start
	- Änderung:hinzugefügt: Attribut hinzugefügt (Datumsbeginn der Bestrahlung)
- Attribut: Procedure.performed.start
	- Änderung: hinzugefügt: Attribut hinzugefügt (Enddatum der Bestrahlung)
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-MedicationStatement-Systemtherapie
- Attribut: MedicationStatement.extension:Protokoll
	- Änderung: hinzugefügt: Extension zur Erfassung das Protokolls der systemischen Therapie hinzugefügt
- Attribut: MedicationStatement.medication.text
	- Änderung: hinzugefügt: Attribut hinzugefügt, um Substanzen zu erfassen

- Attribut: MedicationStatement.effective.start
	- Änderung: hinzugefügt: Attribut hinzugefügt (Datumsbeginn der systemischen Therapie)
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Observation-TodUrsache
	- Änderung: hinzugefügt: neue Observation, um die Todesursache  zu erfassen
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-ClinicalImpression-Verlauf
- Attribut: ClinicalImpression.finding.itemReference
	- Änderung: referenziert: Integration von http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Observation-TodUrsache in das Verlauf-Profil
	- Änderung: referenziert: Integration von http://dktk.dkfz.de/fhir/StructureDefinition/onco-core-Observation-GenetischeVariante in das Verlauf-Profil
----------------------------------------------------

Profil: http://dktk.dkfz.de/fhir/onco/core/ValueSet/TNMTVS
	- Änderung: erweitert: Ausprägungen hinzugefügt (1c1, 1c2, 1c3)